# Black History

[Return to main page](index.md)

### 2016.7.23
Upload 5.6.1-1/5.7.0 VS2015 static builds again due to link issue.

From now on, I will not link MySQL/PostgreSQL/ODBC(unix-like only)/OpenSSL in the static packages.  
The configure scripts may be like this:
```
configure xxxxx -static -openssl -qt-sql-sqlite -no-sql-mysql -no-sql-psql -no-sql-odbc(for unix-like)/-qt-sql-odbc(for windows)
```

I'm anti of static builds, see the notes for details.

### 2016.7.17
Upload all files to Mega.nz for users who are not in China.

### 2016.7.16
Upload 4.8.7 macOS shared packages.

Upload 4.8.7 Linux shared packages.

### 2016.7.15
From now on, I will distribute the config.status(for Unix-like system) or configure.cache(for Windows) in the compressed packages.
config.status contains all my commands when calling configure, while configure.cache only contains the parameters passed to configure.exe.

Upload 4.8.7 VS2015 Shared packages. (And are the first and second packages which have configure.cache)

Update note to suit Qt4.

Update note about QtBinPatcher.

Upload 4.8.7 VS2010 Shared packages.

Update note about old-version Qt.

### 2016.7.4
Upload 5.6.1-1 VS2015 Static packages.

Upload 5.6.1-1 Android(Windows x86_64 host) Shared packages.

Upload 5.6.1-1 VS2010 Shared packages __just for the unreconstructed people using Windows XP__.

Update note.

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
