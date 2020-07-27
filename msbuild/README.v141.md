# OPENSSL.V141

This package contains debug and release builds of the OpenSSL 1.1.1g library. It was built with Visual Studio 2017 (V141).

## Source

The source code used to build this package is available at https://github.com/zeroc-ice/openssl/tree/msvc.

## Build Instructions

git clone git@github.com:zeroc-ice/openssl.git -b msvc
cd openssl

From a Visual Studio 2017 x86 Command promt run the following commands

    MSBuild msbuild\openssl.proj /t:NugetPack /p:Platform=Win32 /p:Configuration=Debug
    MSBuild msbuild\openssl.proj /t:NugetPack /p:Platform=Win32 /p:Configuration=Release

From a Visual Studio 2017 x64 Command promt run the following commands

    MSBuild msbuild\openssl.proj /t:NugetPack /p:Platform=x64 /p:Configuration=Debug
    MSBuild msbuild\openssl.proj /t:NugetPack /p:Platform=x64 /p:Configuration=Release

Then you can create the openssl.v141 nuget package running the following command

    MSBuild msbuild\openssl.proj /t:NugetPack
