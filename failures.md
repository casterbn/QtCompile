# Build Failures about the original packages

[Return to main page](index.md)

## Qt 4.8 can't be built using VS2017/2019

## Qt Webkit 4.8 can't be built using VS2015

## Qt 5.6/5.9 can't be built using VS2019

## Qt WebEngine 5.6 can't be built using VS2017

## Qt 5.12 wasm builds can't built with OpenSSL

Both `qsslsocket_opensslpre11.cpp` and `qsslsocket_openssl11.cpp` includes `qlibrary.h` which is not usable in wasm platform.  
Since `-openssl` and `-openssl-linked` both use this file, so we can only use `-no-ssl`.......

## Qt 5.12 with WebEngine can only be built by hand

Using compile scripts will cause failure. Reason is unknown.

## Default compressed VS2015 static package is detected as malware by SF.net

Recompress it by hand solves the problem.

## Android NDK r20 can't be used for building Qt

`cannot find library -lc++`

## MDWiki can't be tested using recent Firefox

Only for local files.
Remote files are working normally.
