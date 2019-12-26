# Build Failures about the original packages

## Qt 4.8 can't be built using VS2017/2019

I'll do when I have time.

## Qt Webkit 4.8 can't be built using VS2015/VS2017/VS2019

I'll do when I have time.

## Qt 5.6/5.9 can't be built using VS2019

I won't do the modifications.

## Qt WebEngine 5.6 can't be built using VS2017/VS2019

I won't do the modifications.

## Qt 5.12 wasm builds can't built with OpenSSL

Both `qsslsocket_opensslpre11.cpp` and `qsslsocket_openssl11.cpp` includes `qlibrary.h` which is not usable in wasm platform.  
Since `-openssl` and `-openssl-linked` both use this file, so we can only use `-no-ssl`.......

## (_Resolved_) ~~Qt 5.12 with WebEngine can only be built by hand~~

~~Using compile scripts will cause failure. Reason is unknown.~~

## Some of default compressed package is detected as malware by SF.net

Recompress it by hand solves the problem.

## (_Resolved in Qt 5.12.5 and 5.13.1_) ~~Android NDK r20 can't be used for building Qt~~

~~`cannot find library -lc++`~~

## QDoc after Qt 5.12 cannot use static linked clang when using MSVC

It uses "libclang_static.lib" but clang don't provide this one.  
I have decided not provide LLVM-based qdoc until I find a way to static link it.

## Qt 5.9.9 and 5.12.6 cannot be compiled using xcode 11

Some parts don't compile.  
Static lite version and host tools compiles, the cross compiled version compiles.  
5.9 series fails on QtConnectivity, while 5.12 series fails on QtWebEngine.

I think that 5.12 series should be fixed soon, but 5.9 series may not be fixed.

## Qt 5.14.0 cannot be compiled for Android with linked OpenSSL

See [QTBUG-80862](https://bugreports.qt.io/browse/QTBUG-80862)  
qmake is always using aarch64 compiler for checking the availability of OpenSSL libs and fails if target arch is not aarch64.