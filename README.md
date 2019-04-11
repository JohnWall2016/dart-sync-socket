Dart Sync Socket
================

[![Build Status](https://travis-ci.org/google/dart-sync-socket.svg?branch=master)](https://travis-ci.org/google/dart-sync-socket)
[![pub package](https://img.shields.io/pub/v/sync_socket.svg)](https://pub.dartlang.org/packages/sync_socket)

A Dart VM Native Extension and supporting Dart libraries that provide
synchronous socket and HTTP client support.

Installing
----------

Add the following to your pubspec.yaml:
```YAML
  sync_socket: '^1.0.1'
```

Then run 'pub get'.

After getting the package with pub, you will need to build the native extension itself.

To build the shared library on Mac OSX or Linux, run the 'tool/build.sh' script.

To build the DLL on Windows (64 bits):
  - Find and execute "vcvars64.bat" ("C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Auxiliary\Build\vcvars64.bat").
  - Compile "sync_socket_extension.cc" (cl /c /I"E:\dart-sdk\include" /DWIN32 /DDART_SHARED_LIB sync_socket_extension.cc).
  - Link "sync_socket_extension.obj" (link sync_socket_extension.obj /DLL /SUBSYSTEM:WINDOWS /MACHINE:X64 /LIBPATH:"E:\dart-sdk\bin" dart.lib).
  - Copy the "sync_socket_extension.dll" to the directory "lib".

Testing
-------

Follow the instructions above for building the shared library then run tests
as normal.
