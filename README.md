# SimpleCppProj
This repository contains a simple C++ project, demonstrating a useful structure for developing an application using TDD. 

## Goals
 * [ ] Find a project structure which works well with test driven development
 * [ ] Understand CMake and CTest to find a workflow that makes test driven development rewarding
 * [ ] Solidify understanding of CMake

## Building the project
It is a popular practice to create a `build` directory to generate build system files in. This avoids
mixing project binaries and project sources.

To build this project in a unix environment:

```bash
$ pwd
$ /Path/To/SimpleCppProj
$ mkdir build
$ cd build
$ cmake .. # Ask CMake to generate a build environment (default is to use Makefiles)
$ make
```

To generate a different build system, `cmake -G <Generator Name>` can be used (e.g. `cmake -G "Sublime Text 2 - Unix Makefiles" ..`).

Build system generators are constrained by platform.


