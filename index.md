# Fsu0413's Qt builds

## Disclaimer

These binaries built by Fsu0413 are __TOTALLY UNTESTED__, use in your own risk.

The code used is downloaded from [here](http://download.qt.io), I only made necessary changes to the source/generated makefile to pass the build.

__THESE PACKAGE ARE PROVIDED "As is", I have no responsibility that you mess up your things with this binaries.__

Thanks for The Qt Company Ltd. and the programmers of Qt for their fantastic work!!

## Notes on the distributed compressed files

Archive files on Windows host are compressed in 7z format using LZMA2 Algorithm, 7z users should update their 7z to 9.20 or later, WinRAR users should update their WinRAR to 4.00 or later, users of other compression softwares should make sure that LZMA2 is supported by your software. 

Archive files on Linux use GNU tar. Archive files on macOS use bsdtar. They are called as:
```
tar -cJf xxx.tar.xz xxx/
```

## 5.6 Series
Since 5.6 series is LTS, so I will remain support until when Qt ends support of these packages.

[5.6.1-1 Series](5.6.1-1-series.md)

## 5.7 Series
[5.7.0 Series](5.7.0-series.md)

## Update

### 2016.7.4
Upload 5.6.1-1 VS2015 Static packages.

### 2016.7.3
Upload 5.6.1-1 VS2015 Shared packages.
Upload 5.6.1-1 MinGW Shared packages.
Upload 5.6.1-1 Linux packages.
Upload 5.6.1-1 macOS packages.
Removed 5.6.1 packages.
Upload 5.6.1-1 Android(Linux x86_64 host) Shared packages.
Upload 5.6.1-1 Android(macOS x86_64 host) Shared packages.

### 2016.6.29
Upload 5.7.0 Android(Windows x86_64 host) Shared packages.

### 2016.6.28
Upload 5.7.0 Android(Linux x86_64 host) Shared packages.
Upload 5.7.0 Android(macOS x86_64 host) Shared packages.

### 2016.6.27
Update Disclaimer.

### 2016.6.22
Upload 5.7.0 VS2015 Static packages.
Upload 5.7.0 MinGW Shared packages.
VS2015-clang packages failed to build, thus cannot upload.

### 2016.6.19
Upload 5.7.0 VS2015 Shared packages.
Upload 5.7.0 macOS packages.

### 2016.6.18
Upload 5.7.0 Linux packages.
Removed 5.6.0 packages.
Upload 5.6.1 VS2015 Static packages.
