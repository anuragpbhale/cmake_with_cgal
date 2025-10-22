# Starter CMakeLists.txt for C++

[CMake](https://cmake.org/) is a build system for C++ programmers for all platforms.

This project aims to explain a simple cmake based build setup ( on linux (ubuntu) ) for absolute beginners.

Advanced users of cmake can use this as a template for a fresh project.

## What are the prerequisites?

### 1. A C++ compiler

Terminal command to install the gcc compiler :

```
sudo apt install gcc
```

### 2. CMake

Terminal command to install CMake:

```
sudo apt-get -y install cmake
```

## Project Filesystem

* CMakeLists.txt : This file stores all the CMake commands required to build your project.
* src : Short for source folder. The source files(.cpp) that you create for your project reside in this folder.
  Multiple source files can be added to the project as follows:

```
set( SRCS src/Source.cpp src/Source2.cpp src/Source3.cpp )
```

The GLOB functionality can also be used to get all the source files while not naming each one.

```
file( GLOB SRCS "src/*.cpp" )
```

* include : The include folder contains the header files(.h, .hpp) for the project.
* lib : Short for the library folder. User created or third party library source codes are stored in this folder. We leave this folder alone now since library creation is an advanced topic.
* build : This is where the executable is "built". To build and run the project you must move to this folder and give the following commands on the terminal:

```
cd build
cmake ..
make 
./project_name
```

Any I/O file handling from within the program will consider the build folder as the present working directory(pwd).

## Question:

What steps would you take to add a header(.h) and source(.cpp) file to the project?

* Where would you place these files in the project filesystem?
* What changes would you make to the cmake file so that the project now considers these new files for compilation?

The author of this repo recommends CMake for large projects.
