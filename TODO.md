This document lists software that is likely or known to require further patching to enable full retpolines.

If you'd like to help out, please open issues and pull requests as appropriate.

# Uses mere assembly likely to require patching ("simple")

* app-arch/p7zip
* dev-cpp/tbb
* dev-lang/python-3*
* dev-libs/botan
* dev-libs/crypto++
* dev-libs/gmp
* dev-libs/libgcrypt
* dev-libs/libsodium / dev-python/pynacl
* dev-libs/nettle
* dev-libs/nspr
* kde-apps/kwave
* media-libs/avidemux-core / media-libs/avidemux-plugins
* media-libs/libass
* media-libs/libdv
* media-libs/libjpeg-turbo
* media-libs/x264

# Generates processor instructions (compilers, JIT) or otherwise complex

* app-emulation/qemu
* app-emulation/wine-vanilla
* dev-db/mariadb
* dev-lang/ghc
* dev-lang/go
* dev-lang/nasm
* dev-lang/ocaml
* dev-lang/ruby
* dev-lang/spidermonkey
* dev-lang/yasm
* dev-libs/boost
* valgrind.h in dev-libs/glib / dev-libs/re2 / dev-util/gdbus-codegen
* dev-libs/libffi
* dev-libs/libpcre
* dev-python/greenlet
* games-emulation/desmume
* games-emulation/dosbox

# Only on non-AMD64 / non-Linux platforms

* dev-libs/boehm-gc / dev-util/boost-build
* dev-python/cffi
* media-gfx/fontforge
* media-libs/glfw

# To investigate

* app-misc/ca-certificates
* app-misc/reptyr
* dev-embedded/sdcc
* dev-libs/elfutils
* dev-libs/nss
* dev-libs/openssl
* dev-qt/designer
* dev-qt/qt-creator
* dev-qt/qt3support
* dev-qt/qtconcurrent
* dev-qt/qtcore
* dev-qt/qtdbus
* dev-qt/qtdeclarative
* dev-qt/qtgraphicaleffects
* dev-qt/qtgui
* dev-qt/qtmultimedia
* dev-qt/qtnetwork
* dev-qt/qtopengl
* dev-qt/qtprintsupport
* dev-qt/qtquickcontrols
* dev-qt/qtscript
* dev-qt/qtsql
* dev-qt/qtsvg
* dev-qt/qttest
* dev-qt/qttranslations
* dev-qt/qtvirtualkeyboard
* dev-qt/qtwebengine
* dev-qt/qtwebkit
* dev-qt/qtwidgets
* dev-qt/qtxml
* dev-qt/qtxmlpatterns
* dev-scheme/guile
* dev-util/abi-compliance-checker
* dev-util/abi-dumper
* dev-util/android-tools
* dev-util/google-perftools
* dev-util/ltrace
* dev-util/perf
* dev-util/strace
* dev-util/valgrind
* mail-client/thunderbird
* media-libs/flac
* media-libs/gavl
* media-libs/gst-plugins-good
* media-libs/libvpx
* media-libs/mesa
* media-libs/mlt
* media-libs/openh264
* media-libs/sdl2-image (for bundled zlib)
* media-plugins/gst-plugins-dv
* media-plugins/gst-plugins-flac
* media-plugins/gst-plugins-libav
* media-plugins/gst-plugins-oss
* media-plugins/gst-plugins-soup
* media-plugins/gst-plugins-taglib
* media-plugins/gst-plugins-v4l2
* media-plugins/kipi-plugins
* media-sound/audacity
* media-sound/clementine
* media-sound/jack-audio-connection-kit
* media-sound/lame
* media-sound/mpg123
* media-sound/mumble
* media-video/avidemux
* media-video/emovix
* media-video/ffmpeg
* media-video/mplayer
* media-video/mpv
* media-video/transcode
* media-video/vlc
* net-analyzer/wireshark
* net-dns/bind-tools
* net-im/psi
* net-libs/gnutls
* net-libs/nodejs
* net-misc/bfgminer
* net-misc/freerdp
* net-misc/ntp
* net-misc/tigervnc
* net-misc/youtube-dl
* net-print/cups
* net-vpn/tor
* sci-libs/cln
* sci-libs/fftw
* sci-libs/gsl
* sys-apps/busybox
* sys-apps/kexec-tools
* sys-apps/man-pages
* sys-apps/sandbox
* sys-apps/texinfo
* sys-boot/gnu-efi
* sys-boot/grub
* sys-boot/syslinux
* sys-devel/binutils
* sys-devel/clang
* sys-devel/gcc
* sys-devel/gdb
* sys-devel/llvm
* sys-firmware/edk2-ovmf
* sys-firmware/ipxe
* sys-firmware/seabios
* sys-fs/multipath-tools
* sys-kernel/linux-firmware
* sys-libs/binutils-libs
* sys-libs/compiler-rt
* sys-libs/compiler-rt-sanitizers
* sys-libs/db
* sys-libs/glibc
* sys-libs/libomp
* sys-libs/libunwind
* sys-libs/zlib
* sys-process/psmisc
* www-client/chromium
* www-client/firefox
* x11-base/xorg-server
* x11-libs/cairo
* x11-libs/gdk-pixbuf
* x11-libs/pixman
* x11-libs/wxGTK
* x11-themes/adwaita-icon-theme
