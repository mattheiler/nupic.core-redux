# nupic.core-redux
Nupic.Core C++ Extraction Redux.

## Quick Start

### Windows

#### Setup

* [CMake](https://cmake.org/download/)
* [VCPKG](https://github.com/Microsoft/vcpkg#quick-start)
* [CapnProto](https://capnproto.org/install.html)

#### Install

* Run `vcpkg install boost`.
* Build the CapnProto `INSTALL` project.  

#### CMake
* Configure
  * Specify the generator for this project: __Visual Studio 15 2017__
  * Specify toolchain file for cross-compiling: __~\vcpkg\scripts\buildsystems\vcpkg.cmake__
* Generate

## Considerations

#### Flatten the file structure? 

* Should internal and external sources be separate?
* There should probably be a CMakeLists.txt in the root, regardless.

```
\nupic.core
  \nupic.core
  CMakeLists.txt
```

#### Project per existing subfolder?

* No redundant, matching filters.
* More modular.
* Many libraries.

```
\nupic.core
  \nupic.algorithms
    \bindings
      Foo.i
    \include
      Foo.hpp
    \src
      Foo.cpp
    \tests
    CMakeLists.txt
  \nupic.encoders
    \bindings
      Bar.i
    \include
      Bar.hpp
    \src
      Bar.cpp
      Qux.cpp
      Qux.hpp
    \tests
    CMakeLists.txt
  ...
  CMakeLists.txt
```
