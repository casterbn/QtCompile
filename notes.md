# Notes for this repo

## Notes on the distributed compressed files

Archive files on Windows host are compressed in 7z format using LZMA2 Algorithm, 7z users should update their 7z to 9.20 or later, WinRAR users should update their WinRAR to 4.00 or later, users of other compression softwares should make sure that LZMA2 is supported by your software. 

Archive files on Linux use GNU tar. Archive files on macOS use bsdtar. They are called as:
```
tar -cJf xxx.tar.xz xxx/
```

## Difference of this Qt and offically distributed Qt

All builds here have been configured with -no-icu, because I thought that the ICU is useless for common users, and it is rather a big thing.

Windows and Android builds are using statically linked OpenSSL/LibreSSL.

No debug libs, which cuts more than half of the size of the whole Qt library.

No examples, which cuts more than a half of the size of the whole Qt library.

Use ANGLE for OpenGL support in Windows builds.

## Notes for downloading file from Baidu Netdisk for users who don't recognize Chinese

The download page of Baidu Netdisk looks like below:

![pic](baidu_netdisk.png)

Just click the button and the download will start.
