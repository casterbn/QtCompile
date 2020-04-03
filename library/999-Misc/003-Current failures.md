# Build Failures about the original packages

## Qt 5.12 wasm builds can't built with OpenSSL

Both `qsslsocket_opensslpre11.cpp` and `qsslsocket_openssl11.cpp` includes `qlibrary.h` which is not usable in wasm platform.  
Since `-openssl` and `-openssl-linked` both use this file, so we can only use `-no-ssl`.......

I didn't try with Qt 5.14 series.

## Some of default compressed package is detected as malware by SF.net

Recompress it by hand solves the problem.

## QDoc after Qt 5.12 cannot use static linked clang when using MSVC

It uses "libclang_static.lib" but clang don't provide this one.  
I have decided not provide LLVM-based qdoc until I find a way to static link it.

## macOS version of QtWebEngine 5.14.2 does not compile

gn compile failed on macOS using xcode 11.4.

## Resolved failures

### (_Resolved_) ~~Qt 5.12 with WebEngine can only be built by hand~~

~~Using compile scripts will cause failure. Reason is unknown.~~

### (_Resolved in Qt 5.12.5 and 5.13.1_) ~~Android NDK r20 can't be used for building Qt~~

~~`cannot find library -lc++`~~

### Qt 5.9.9 ~~and~~ (_Resolved in Qt 5.12.7_) ~~5.12.6~~ cannot be compiled using xcode 11

Some parts don't compile.  
Static `lite` version and host tools compiles, the cross compiled version compiles.  
5.9 series fails on QtConnectivity~~, while 5.12 series fails on QtWebEngine~~.

I think that ~~5.12 series should be fixed soon, but~~ 5.9 series may not be fixed.  
I ~~will use~~ used xcode 11 for compiling 5.12.7. QtWebEngine has successfully compiled. ~~Certain parts will be skipped if they don't compile.~~

### (_Resolved in Qt 5.14.1_) ~~Qt 5.14.0 cannot be compiled for Android with linked OpenSSL~~

~~See [QTBUG-80862](https://bugreports.qt.io/browse/QTBUG-80862)~~  
~~qmake is always using aarch64 compiler for checking the availability of OpenSSL libs and fails if target arch is not aarch64.~~

### (_Resolved_ by adding some options in command line) ~~Default compressed package is often 1.5~2 times larger than manually compressed ones~~

~~Notably in static `full` packages which often reach 150MB+.~~

~~I use more dictionary size and word size in the compress setting dialog.~~
~~Since it will use more memory, I didn't use it in scripts.~~
~~I will try to add the dictionary size and word size option in the compress command line when I have time.~~

### (_Resolved_) ~~QtWebEngine does not compile on 5.15.0 beta versions on Windows platforms~~

It was because of the 260-character limitation on Windows.
Change the extract path on Windows solves this problem.

## (_Resolved_) ~~Qt 5.14.1 can't be compiled using NDK r21~~

~~It is said that~~ Qt 5.14.2 resolved this issue.
