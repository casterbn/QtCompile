# 5.6.3 Series

[Return to main page](index.md)

Note: ODBC and SQLite(distributed with Qt) are built in the backage. All Dynamic builds have -plugin-sql-xxx.

Note: Windows(except static ver2) builds have -openssl-linked,  
for Windows it is linked to a static openssl(libssl.a/libcrypto.a/ssleay32.lib/libeay32.lib),   

Note: All builds have -no-icu because I think the ICU library is too big and, in most of time, useless for common users.

## Dynamic / Shared Builds

### Windows

VS2015 and MinGW builds targets Windows 7 or later, VS2010 builds targets the __old-fashioned XP__

Visual Studio 2015 Update 3(__WITHOUT__ KB3165756), ANGLE(es2)

Build host: Windows 7 SP1

Qt5.6.1-1-Windows-x86-VS2015.7z [Baidu Netdisk](http://pan.baidu.com/s/1eRRa3sQ) [Mega](https://mega.nz/#!oExTTDIS!RFNwlTNqir6h_BGxkagLGHkzdYMQCYPk10itS6Gkzh4)

Qt5.6.1-1-Windows-x86_64-VS2015.7z [Baidu Netdisk](http://pan.baidu.com/s/1pLpKDYj) [Mega](https://mega.nz/#!ZJYAHJrQ!WAAKDptGu__aJmQ5ZnxmmXHBQIqi0_6DUy0OdthdkSs)

MinGW-w64 from sf.net, ANGLE(es2), __NO WEBENGINE/WEBVIEW__

Build host: Windows 7 SP1

Qt5.6.1-1-Windows-x86-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1jIAnBz4) [Mega](https://mega.nz/#!ZFwGUKpR!fG4WHP8o_OvAxGUbpnf___XzR2hpJXEtrrJ3A9YsC1Q)

Qt5.6.1-1-Windows-x86_64-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1bpiH6Pp) [Mega](https://mega.nz/#!FVo2lSCQ!m5cfulkIUz9Bxav28uNOwBzeg_JtSOCUUc6vR7jidyw)

Visual Studio 2010 SP1, Windows SDK 7.0A, ANGLE(es2), __XP COMPATIBLE, NO WEBENGINE/WEBVIEW, NO MYSQL/PSQL, 32-bit ONLY, just for the unreconstructed people who want to use XP eagerly__.

Build host: Windows XP SP3

Qt5.6.1-1-Windows-x86-VS2010.7z [Baidu Netdisk](http://pan.baidu.com/s/1dF1AwMX) [Mega](https://mega.nz/#!hQpHXRIQ!LeGhqotSV-FcUxYEq2j2SGINvoS420qDhc5v6S5y-hA)

### macOS / OS X

Using newest XCode in OS X 10.11.5

Qt5.6.1-1-macOS-x86_64-Clang7.3.0-framework.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1o7HWIOq) [Mega](https://mega.nz/#!hUAmDCaQ!ds4keLK9xaJFXFfMJ5oHVZyEMIt-G8VHmzQg90SVGeM)  Framework

Qt5.6.1-1-macOS-x86_64-Clang7.3.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1nuC9cMl) [Mega](https://mega.nz/#!wERFHAwL!yxG5IS8ABZkCgtXpFu524GOyoH3z6zKp9g4xXnToylc)  No-Framework

### Android

[Here](5.6.1-1-android.md)

## Static builds

### Windows

VS2015 and MinGW builds targets Windows 7 or later, VS2010 builds targets the __old-fashioned XP__

Visual Studio 2015 Update 3(__WITHOUT__ KB3165756), ANGLE(es2)

Build host: Windows 7 SP1

Qt5.6.1-1-Windows-x86-VS2015.7z [Baidu Netdisk](http://pan.baidu.com/s/1eRRa3sQ) [Mega](https://mega.nz/#!oExTTDIS!RFNwlTNqir6h_BGxkagLGHkzdYMQCYPk10itS6Gkzh4)

Qt5.6.1-1-Windows-x86_64-VS2015.7z [Baidu Netdisk](http://pan.baidu.com/s/1pLpKDYj) [Mega](https://mega.nz/#!ZJYAHJrQ!WAAKDptGu__aJmQ5ZnxmmXHBQIqi0_6DUy0OdthdkSs)

MinGW-w64 from sf.net, ANGLE(es2), __NO WEBENGINE/WEBVIEW__

Build host: Windows 7 SP1

Qt5.6.1-1-Windows-x86-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1jIAnBz4) [Mega](https://mega.nz/#!ZFwGUKpR!fG4WHP8o_OvAxGUbpnf___XzR2hpJXEtrrJ3A9YsC1Q)

Qt5.6.1-1-Windows-x86_64-MinGW5.4.0.7z [Baidu Netdisk](http://pan.baidu.com/s/1bpiH6Pp) [Mega](https://mega.nz/#!FVo2lSCQ!m5cfulkIUz9Bxav28uNOwBzeg_JtSOCUUc6vR7jidyw)

Visual Studio 2010 SP1, Windows SDK 7.0A, ANGLE(es2), __XP COMPATIBLE, NO WEBENGINE/WEBVIEW, NO MYSQL/PSQL, 32-bit ONLY, just for the unreconstructed people who want to use XP eagerly__.

Build host: Windows XP SP3

Qt5.6.1-1-Windows-x86-VS2010.7z [Baidu Netdisk](http://pan.baidu.com/s/1dF1AwMX) [Mega](https://mega.nz/#!hQpHXRIQ!LeGhqotSV-FcUxYEq2j2SGINvoS420qDhc5v6S5y-hA)

### macOS / OS X

Using newest XCode in OS X 10.11.5

Qt5.6.1-1-macOS-x86_64-Clang7.3.0-framework.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1o7HWIOq) [Mega](https://mega.nz/#!hUAmDCaQ!ds4keLK9xaJFXFfMJ5oHVZyEMIt-G8VHmzQg90SVGeM)  Framework

Qt5.6.1-1-macOS-x86_64-Clang7.3.0.tar.xz [Baidu Netdisk](http://pan.baidu.com/s/1nuC9cMl) [Mega](https://mega.nz/#!wERFHAwL!yxG5IS8ABZkCgtXpFu524GOyoH3z6zKp9g4xXnToylc)  No-Framework
