# 5.6.3 Series for Android

[Return to 5.6.3 Series](5.6.3-series.md)

Note: SQLite(distributed with Qt) are built in the backage and have -plugin-sql-sqlite

Note: All packages have -openssl-linked, Since BoringSSL, which is used in Android 6.0 or later, is NOT API COMPATIBLE WITH OPENSSL, we link it to a static OpenSSL instead of system SSL library. 

Note: All builds have -no-icu because I think the ICU library is too big and, in most of the conditions, useless for common users.

Note: All builds are using NDK r10e with -android-ndk-platform android-9, it means the APK built using these packages may be not able to run on Android 2.3.x and earlier.

## Dynamic Builds

### Windows Host

Build host: Windows 10 Pro Insider Preview

Note: Built using 64-bit NDK and 64-bit MinGW, make sure you are using 64-bit windows and have 64-bit MinGW 5.4.0(I redistribute it in the MinGW packages) installed, and mingw32-make.exe in PATH.

Qt5.7.0-Android-arm-gcc4.9.0XWindows-x86_64-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1hrVFUa4) [Mega](https://mega.nz/#!ZFxwwbbJ!ojQRP8QJkocFyepOlCKi4tx1jDEYmAPDR0Yzenmcds4)

Qt5.7.0-Android-arm64-gcc4.9.0XWindows-x86_64-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1gfdP0lH) [Mega](https://mega.nz/#!IAATCKgC!9vkNjUEXjFICTP7zhupq0K_kAF9ty_942FkjPucv1bw)

Qt5.7.0-Android-x86-gcc4.9.0XWindows-x86_64-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1eRMq76a) [Mega](https://mega.nz/#!UF4FBQaK!Edsaf7897QGlxIxfpKSlM-ZCGTvgdsUxcHosE3_AQ68)

Qt5.7.0-Android-x86_64-gcc4.9.0XWindows-x86_64-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1eRH6ROe) [Mega](https://mega.nz/#!cZJzBYJZ!mROqEztVbr26XTWR32JDuUIwZHHpK72e07RWm51R9Lk)

Qt5.7.0-Android-mips-gcc4.9.0XWindows-x86_64-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1dEVgbVr) [Mega](https://mega.nz/#!5EoDQASS!E_KAuukNUwc6DHnRQa-Id3TGWFvg00VbZuPoAty0PRs)

Qt5.7.0-Android-mips64-gcc4.9.0XWindows-x86_64-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1bpbpJL9) [Mega](https://mega.nz/#!0cInWaTS!lCXknKDyyRrqtTJkdo4k5R2XDlURkybxTL-jWSVyz4Q)

### Linux Host

Build host: Debian testing, with "apt-get update && apt-get dist-upgrade" run before building

Qt5.7.0-Android-arm-gcc4.9.0Xlinux-x86_64-gcc5.4.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1pLfAYD1) [Mega](https://mega.nz/#!wF4zjQJI!QRxcRRvZ1v7YNVNRofsiQ0HnOYHeHxmZiThRuzA876k)

Qt5.7.0-Android-arm64-gcc4.9.0Xlinux-x86_64-gcc5.4.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1c16L5jM) [Mega](https://mega.nz/#!dUYTiATb!Rd0j0sVzh0Ekc7TPz5Om282VmAWSdSehAMZtNKyw9g0)

Qt5.7.0-Android-x86-gcc4.9.0Xlinux-x86_64-gcc5.4.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1eREOX9K) [Mega](https://mega.nz/#!5Uo1UI6L!Z6GbG9nmF_NGEU7ebe3jQXypu8UHzGCSO2g2qP8arvQ)

Qt5.7.0-Android-x86_64-gcc4.9.0Xlinux-x86_64-gcc5.4.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1c1XjV48) [Mega](https://mega.nz/#!9JRVFKja!BgGqpRZOz9ooQ6vRPW05S0atPIDOGWCZVTusR96-aS4)

Qt5.7.0-Android-mips-gcc4.9.0Xlinux-x86_64-gcc5.4.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1jH7pprg) [Mega](https://mega.nz/#!xcQSzICa!8Wqs2tyX-Ytw2wF9QeM2Tbi_GfsFOtZXfIDScuzqNpk)

Qt5.7.0-Android-mips64-gcc4.9.0Xlinux-x86_64-gcc5.4.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1i511TdV) [Mega](https://mega.nz/#!dQBDAYgJ!GNpRGq_BzXF2Fyc78XfXLjVkKGUQA_LCqmzLU-6iEPk)

### macOS Host

Using newest XCode in OS X 10.11.5

Qt5.7.0-Android-arm-gcc4.9.0XMacOS-x86_64-clang7.3.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1sk8wTwp) [Mega](https://mega.nz/#!9Io22LAC!ohIHzogLUc_KoJxQUUgcdB7nbr0I_krE4IYyGDG6Rks)

Qt5.7.0-Android-arm64-gcc4.9.0XMacOS-x86_64-clang7.3.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1eRF4UyQ) [Mega](https://mega.nz/#!FUYVGQDI!4LKFQ1fN5ABIPHt9aFWoIfWb8E3mXAcRPV2fFDwvrQQ)

Qt5.7.0-Android-x86-gcc4.9.0XMacOS-x86_64-clang7.3.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1dE2FJtZ) [Mega](https://mega.nz/#!tcASEIbJ!LvFxqTHi4HC01DPrOlxy7U5T46OmDdyYmh9gmyZMmCE)

Qt5.7.0-Android-x86_64-gcc4.9.0XMacOS-x86_64-clang7.3.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1i5uGueL) [Mega](https://mega.nz/#!tBpUzTjA!JVXllwNzXpKTaHJZ_M7QJayBG14KyNGWSzegRerQTLk)

Qt5.7.0-Android-mips-gcc4.9.0XMacOS-x86_64-clang7.3.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1hrPAnGS) [Mega](https://mega.nz/#!AIwXSJ7D!NBkA86B-0_lGjrpB4BXQUTWy_oD43so8ChsrFcRG41Q)

Qt5.7.0-Android-mips64-gcc4.9.0XMacOS-x86_64-clang7.3.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1hspsGqK) [Mega](https://mega.nz/#!lFxhEJJT!pLmVDKOUgObmqFNgaXjjUf93IgC8REgnDUsLsPwt8xA)
