These patches enable and help enforce building your entire system with retpolines.
It is designed for Gentoo, but may be useful on other built-from-source systems as well.

Note that this is *intentionally* excessive: certain compile flags are enabled that may very well be unnecessary.
In particular, -O0 and -Og will throw an error by default.

# GCC: Usage, caution

The GCC patches enable all retpolines by default, and modifies the defaults for other CFLAGS that are suspected at taking away from its protections.
It also tries to prevent changing these defaults without also explicitly disabling the retpolines:
-O1, -fearly-inlining (upstream default), -fgcse (enabled in -O2 upstream), -fgcse-lm (upstream default), -finline (upstream default), and -finline-small-functions (enabled in -O2 upstream).
-Og is also prevented.

Since common CFLAGS are prohibited, this can cause problems with some build systems, especially ones that test availability of certain features with an unnecessary -O0 flag (they may assume the feature in question is not present, rather than aborting the build).

For this reason, forbidden CFLAGS do not cause GCC to abort.
Instead, it sends itself SIGSTOP to freeze the process, and puts a message in the syslog.
(I recommend configuring your syslog to alert you to such messages so you know it is waiting on your interaction.)
At that point, you may either permit it to continue by sending SIGCONT, or you can send SIGKILL to forcefully terminate it (as a failure).

You can disable CFLAGS limitations entirely by setting LJR_BYPASS_RETPOLINE=1 in the environment.

# libgcrypt

libgcrypt by default builds the Jitter 100% software RNG.
The upstream author cautions that the RNG must be compiled without optimisations, or will be insecure (low entropy).
For this reason, libgcrypt is patched to entirely disable the Jitter RNG by default.

# libgpg-error

For unknown reasons, a build-time tool `mkheader` was compiled with -O0.
It seems fairly safe to let it get optimised, so the patch simply removes -O0.

# Linux kernel

To build a kernel, add a GNUmakefile with (adjust the path to this git repo):

```
CROSS_COMPILE=/path/to/gcc-no-retpoline/x86_64-pc-linux-gnu-no-retpoline-
include Makefile
```

NOTE: If you were using the older steps for the kernel, be sure to *remove* the patch!

This will effectively undo the main changes of this patch for the kernel's build system.
Since the kernel has its own retpoline support, this should be safe.
