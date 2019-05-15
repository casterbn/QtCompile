# Current Status

[Return to main page](index.md)

## QQtPatcher Support Status

This is a list which QQtPatcher is supported and tested on.  
Other version may work, but also may silently fail.

A valid qbp.json is needed for patching Qt 4 Series since `qmake -query` don't output the makespec.

| Qt Version | -platform | -xplatform | Notes |
|-|
|4.8.7|win32-msvc2010|-|Needs qbp.json|
|4.8.7|win32-g++|-|Needs qbp.json|
|4.8.7|macx-llvm|-|Needs qbp.json|
|5.6.3|win32-msvc2010|-||
|5.6.3|win32-msvc2015|-||
|5.6.3|win32-g++|-||
|5.6.3|win32-g++|android-g++||
|5.6.3|macx-clang|-||
|5.6.3|linux-g++|-||
|5.6.3|linux-g++|android-g++||
|5.9.8|win32-msvc|-|VS2015, VS2017|
|5.9.8|win32-g++|-||
|5.9.8|win32-g++|android-g++||
|5.9.8|macx-clang|-||
|5.9.8|linux-g++|-||
|5.9.8|linux-g++|android-g++||
|5.12.3|win32-msvc|-|VS2015, VS2017, VS2019|
|5.12.3|win32-g++|-||
|5.12.3|win32-g++|android-clang||
|5.12.3|macx-clang|-||
|5.12.3|linux-g++|-||
|5.12.3|linux-g++|android-clang||
|5.12.3|linux-g++|wasm-emscripten||

Build Hosts:

| Qt Version | -platform | Host | Compiler Version |
|-|
|5.6.3|win32-g++|Windows XP SP3|MinGW 4.9.4|
|5.6.3|macx-clang|OS X 10.10|AppleClang 6.1|
|5.12.3|win32-msvc|Windows Server 2008 R2 SP1|VS2015 Update 3|
|5.12.3|win32-msvc|Windows 10 10.0.17763|VS2017 15.9.11|
|5.12.3|macx-clang|macOS 10.14|AppleClang 10.0|
|5.12.3|linux-g++|CentOS 7.5|GCC 4.8.5|
|5.12.3|linux-g++|Ubuntu 16.04|GCC 5.4.0|

## Qt 4.8.7 Series

| Platform | Build Host | Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows XP SP3|VS2010 SP1|x86||win32-msvc2010|√|√|
|↑|↑|MinGW 4.9.4|x86||win32-g++|√|√|
|macOS|OS X 10.10|AppleClang 6.1|x86_64|-framework|macx-llvm||√|
|↑|↑|↑|x86_64|-no-framework|macx-llvm||√|

## Qt 5.6.3 Series

| Platform | Build Host | Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows XP SP3|VS2010 SP1|x86||win32-msvc2010|√|√|
|↑|↑|↑|x86|-static|win32-msvc2010|√|√|
|↑|↑|↑|x86|-static(Full)|win32-msvc2010|√|√|
|↑|Windows Server 2008 R2 SP1|VS2015 Update 3|x86||win32-msvc2015|√|√|
|↑|↑|↑|x86|-target xp|win32-msvc2015|√|√|
|↑|↑|↑|x86_64||win32-msvc2015|√|√|
|↑|Windows XP SP3|MinGW 4.9.4|x86||win32-g++|√|√|
|↑|Windows Server 2008 R2 SP1|↑|x86_64||win32-g++|√|√|
|↑|Windows XP SP3|↑|x86|-static|win32-g++|√|√|
|↑|↑|↑|x86|-static(Full)|win32-g++|√|√|
|macOS|OS X 10.10|AppleClang 6.1|x86_64|-framework|macx-clang||√|
|↑|↑|↑|x86_64|-no-framework|macx-clang||√|
|↑|↑|↑|x86_64|-static|macx-clang|Won't upload|√|
|Android|Windows 10 10.0.17763|ndk r10e|arm||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|
|↑|CentOS 7.5|↑|arm||android-g++||√|
|↑|↑|↑|x86||android-g++||√|
|↑|OS X 10.10|↑|arm||android-g++|||
|↑|↑|↑|x86||android-g++|||

## Qt 5.9.8 Series

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows Server 2008 R2 SP1|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.17763|VS2017 15.9.11|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows Server 2008 R2 SP1|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|macOS|macOS 10.14|AppleClang 10.0|x86_64|-framework|macx-clang||√|
|↑|↑|↑|x86_64|-no-framework|macx-clang||√|
|Android|Windows 10 10.0.17763|ndk r10e|arm||android-g++|√|√|
|↑|↑|↑|arm64||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|
|↑|CentOS 7.5|↑|arm||android-g++||√|
|↑|↑|↑|arm64||android-g++|||
|↑|↑|↑|x86||android-g++||√|
|↑|macOS 10.14|↑|arm||android-g++|||
|↑|↑|↑|arm64||android-g++|||
|↑|↑|↑|x86||android-g++|||

## Qt 5.12.3 Series

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows Server 2008 R2 SP1|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86|-static|win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.17763|VS2017 15.9.11|x86||win32-msvc|√|√|
|↑|↑|↑|x86|-static|win32-msvc|√|√|
|↑|↑|↑|x86|-static(Full)|win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|↑|↑|x86_64|-static(Full)|win32-msvc|√|√|
|↑|↑|VS2019 16.0.3|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows Server 2008 R2 SP1|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|Linux|CentOS 7.5|GCC 4.8.5|x86_64|-static|linux-g++|Won't upload||
|↑|Ubuntu 16.04|GCC 5.4.0|x86_64|-static|linux-g++|Won't upload||
|macOS|macOS 10.14|AppleClang 10.0|x86_64|-framework|macx-clang||√|
|↑|↑|↑|x86_64|-no-framework|macx-clang||√|
|↑|↑|↑|x86_64|-static|macx-clang|Won't upload|√|
|Android|Windows 10 10.0.17763|ndk r19c|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|↑|CentOS 7.5|↑|arm||android-clang||√|
|↑|↑|↑|arm64||android-clang||√|
|↑|↑|↑|x86||android-clang||√|
|↑|macOS 10.14|↑|arm||android-clang|||
|↑|↑|↑|arm64||android-clang|||
|↑|↑|↑|x86||android-clang|||
|WebAssembly|Ubuntu 16.04|emscripten-1.38.16|-||wasm-emscripten||√|
|↑|macOS 10.14|↑|-||wasm-emscripten|||

## Qt 5.13.0 Series

Qt 5.13.0 will release in May.

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows Server 2008 R2 SP1|VS2015 Update 3|x86||win32-msvc||√|
|↑|↑|↑|x86_64||win32-msvc||√|
|↑|Windows 10 10.0.17763|VS2017 15.9.11|x86||win32-msvc||√|
|↑|↑|↑|x86_64||win32-msvc||√|
|↑|↑|VS2019 16.0.3|x86||win32-msvc||√|
|↑|↑|↑|x86_64||win32-msvc||√|
|↑|↑|MinGW 7.3.0|x86||win32-g++||√|
|↑|↑|↑|x86_64||win32-g++||√|
|macOS|macOS 10.14|AppleClang 10.0|x86_64|-framework|macx-clang||√|
|↑|↑|↑|x86_64|-no-framework|macx-clang||√|
|Android|Windows 10 10.0.17763|ndk r19c|arm||android-clang||√|
|↑|↑|↑|arm64||android-clang||√|
|↑|↑|↑|x86||android-clang||√|
|↑|CentOS 7.5|↑|arm||android-clang||√|
|↑|↑|↑|arm64||android-clang||√|
|↑|↑|↑|x86||android-clang||√|
|↑|macOS 10.14|↑|arm||android-clang|||
|↑|↑|↑|arm64||android-clang|||
|↑|↑|↑|x86||android-clang|||
|WebAssembly|Windows 10 10.0.17763|emscripten-1.38.27|-||wasm-emscripten|||
|↑|Ubuntu 16.04|↑|-||wasm-emscripten|||
|↑|macOS 10.14|↑|-||wasm-emscripten|||

