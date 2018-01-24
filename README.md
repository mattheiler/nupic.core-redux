# nupic.core-redux
Nupic.Core C++ Extraction Redux.

## Quick Start

### Windows

#### Setup

* [CMake](https://cmake.org/download/)
* [VCPKG](https://github.com/Microsoft/vcpkg#quick-start)

#### Install

* Run `vcpkg install boost`.
* Run `vcpkg install yaml-cpp`.
* Run `vcpkg install zlib`. 

#### CMake

I used the Windows GUI.

* __CONFIGURE__
  * Specify the generator for this project: __Visual Studio 15 2017__
  * Specify toolchain file for cross-compiling: __~\vcpkg\scripts\buildsystems\vcpkg.cmake__
* __GENERATE__
