# Notes for this repo

[Return to main page](index.md)

## Notes on the distributed compressed files

Archive files on Windows host are compressed in 7z format using LZMA2 Algorithm,   
7z users should update their 7z to 9.20 or later,   
WinRAR users should update their WinRAR to 4.00 or later,   
users of other compression softwares should make sure that LZMA2 is supported by your software.

Archive files on Linux use GNU tar. Archive files on macOS use bsdtar. They are called as:
```
tar -cJf xxx.tar.xz xxx/
```

## Difference of this Qt and offically distributed Qt

All Qt 5 builds here have been configured with -no-icu, because I thought that the ICU is useless for common users, and it is rather a big thing.  
Another reason is that Qt5 have depecrated WebKit, which depends on ICU.

Windows/Android builds are using statically linked OpenSSL/LibreSSL.

No debug libs, which cuts more than a half of the size of the whole Qt library.

No examples, which cuts more than a half of the size of the whole Qt library.

No demos for Qt 4 builds, which cuts more than a half of the size of the whole Qt library.

Use ANGLE for OpenGL support in Windows Qt 5 builds instead of dynamically loading the OpenGL libs.

## Notes for downloading file from Baidu Netdisk for users who don't recognize Chinese

The download page of Baidu Netdisk looks like below:

![pic](baidu_netdisk.png)

Just click the button and the download will start.

## Notes for Qt Creator users

Qt Creator should complain about the just uncompressed binary file, and says "Qt is not properly installed, please run _make install_" or something like this.

I redistributed a version of QtBinPatcher, you should run it to make Qt Creator running.

The source code of the distributed QtBinPatcher is on [Github](https://github.com/Fsu0413/QtBinPatcher). It is a free software and distributed in public domain.
