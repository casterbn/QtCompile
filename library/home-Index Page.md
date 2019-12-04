# Fsu0413's Original Qt builds

## Disclaimer

These binaries built by Fsu0413 are __TOTALLY UNTESTED__. Use at your own risk.

The code used is downloaded from [here](http://download.qt.io), I made no changes to the source/generated files.

__THESE PACKAGE ARE PROVIDED "As is", I have no responsibility that you mess up your things with this binaries.__

Thanks for The Qt Company Ltd. and the programmers of Qt for their fantastic work!!

## Notes for this repo

[here](?file=008-Misc/001-Notes%20for%20this%20repo)

## Current build status

[here](?file=008-Misc/002-Current%20build%20status)

## Downloads
Please refer to the content lists in the left area.

## Current failures

[here](?file=008-Misc/003-Current%20failures)

## Update

### 2019.12.2

Uploaded all rebuilt packages after my business trip.

### 2019.11.22
Update pending after I return to China.....  
Qt 5.12 Series => 5.12.6  
Qt 5.13 Series => 5.13.2 -> prepare to migrate to Qt 5.14 Series  
OpenSSL 1.0.2 Series => OpenSSL 1.0.2t (affects Qt 4.8/5.6/5.9 Series)  
OpenSSL 1.1.1 Series => OpenSSL 1.1.1d (affects Qt 5.12/5.13 Series)  
VS2017 => 15.9.17  
VS2019 => 16.3.10  
Andrid NDK => r20b

OS update pending.....  
Win10 => 10.0.18363  
CentOS 7 => 7.7.1908 (Should there be a CentOS 8 environment? Currently Ubuntu 16.04 LTS is used to build the WebAssembly packages. If we change to CentOS 8 then it will become based on new software)  
macOS 10.14 => 10.15

There will be no further build of original Qt 4.8/5.6 after OpenSSL 1.0.2 Series gets EOL (will be at 2019.12.31)  
There will be no further build of original Qt 5.9 after Qt 5.9 Series gets EOL (will be at 2020.5.31)  
There will be no build on Windows 7 (Server 2008 R2) after Windows 7 gets EOL (will be at 2020.1.11), existing Windows 7 builds will migrate to Windows 8.1 (Server 2012 R2)

### 2019.8.26
A bug about packaging has been revealed. It affects all versions of Qt 5.12 or later.  
The package of 5.12.5 will fix this issue.

### 2019.8.3
Re-create this site using amWiki.  
Since there is a builtin content list when using amWiki, it no longer needs to write the downloadable content list manually by now.

### 2019.7.13
Rebuild __ALL__ packages using updated QQtPatcher due to a bug in QQtPatcher.  
VS2017 is updated to 15.9.14.  
VS2019 is updated to 16.1.6.

### 2019.7.9
WebAssembly packages are updated to Qt 5.12.4 and Qt 5.13.0.

### 2019.7.8
Android packages are updated to Qt 5.12.4 and Qt 5.13.0. <font color=red>__Used NDK r19c, although the file name is r20__</font>  
Rebuild Android packages with OpenSSL 1.1.1c and 1.0.2s.  
Page links to Android/Wasm packages are put into main page instead of the "XXX-series" pages.

### 2019.7.6
Windows packages are updated to Qt 5.13.0.

### 2019.7.5
Rebuild Windows packages with OpenSSL 1.1.1c and 1.0.2s.  
Windows packages are updated to Qt 5.12.4.

### 2019.5.26
Rebuild VS2017/VS2019 packages with update VS version.

### 2019.5.19
Linux hosted Android packages rebuilt with updated configurations.  
Upload Linux hosted WebAssembly package(No 's'...)  
Since SF.net reworked, the files are reuploaded to SF.net.

(Why can't I use SFTP to manage the files on OSDN?????)

### 2019.5.15
Windows packages rebuilt with updated configurations.  
Since SF.net can't be accessed using China Telecom in Dalian, China, the files are reuploaded to OSDN.

### 2019.4.22
Upload 5.9.8 and 5.12.3 VS2015 packages.

### 2019.4.20
Finish 5.9.8 and 5.12.3 series.

### 2019.4.19
Removed All old packages.  
Upload new packages built since Mar, 2019.