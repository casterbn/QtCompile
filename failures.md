# Build Failures about the original packages

[Return to main page](index.md)

## Qt 4.8 can't be built using VS2017/2019

## Qt Webkit 4.8 can't be built using VS2015

## Qt 5.6/5.9 can't be built using VS2019

## Qt Webengine 5.6 can't be built using VS2017

## Qt 5.12 wasm builds can't built with openssl

Both `qsslsocket_opensslpre11.cpp` and `qsslsocket_openssl11.cpp` includes `qlibrary.h` which is not usable in wasm platform.  
Since `-openssl` and `-openssl-linked` both use this file, so we can only use `-no-ssl`.......
