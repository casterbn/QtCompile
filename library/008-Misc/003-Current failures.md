# Build Failures about the original packages

## Qt 4.8 can't be built using VS2017/2019

## Qt Webkit 4.8 can't be built using VS2015/VS2017/VS2019

## Qt 5.6/5.9 can't be built using VS2019

## Qt WebEngine 5.6 can't be built using VS2017/VS2019

## Qt 5.12 wasm builds can't built with OpenSSL

Both `qsslsocket_opensslpre11.cpp` and `qsslsocket_openssl11.cpp` includes `qlibrary.h` which is not usable in wasm platform.  
Since `-openssl` and `-openssl-linked` both use this file, so we can only use `-no-ssl`.......

## (_Resolved_) ~~Qt 5.12 with WebEngine can only be built by hand~~

~~Using compile scripts will cause failure. Reason is unknown.~~

## Some of default compressed package is detected as malware by SF.net

Recompress it by hand solves the problem.

## (_Resolved in Qt 5.12.5 and 5.13.1_) ~~Android NDK r20 can't be used for building Qt~~

~~`cannot find library -lc++`~~
