# C++ Boilerplate
[![Build Status](https://travis-ci.org/vijay4313/Week4_TDD_4B.svg?branch=master)](https://travis-ci.org/vijay4313/Week4_TDD_4B)
[![Coverage Status](https://coveralls.io/repos/github/vijay4313/Week4_TDD_4B/badge.svg?branch=master)](https://coveralls.io/github/vijay4313/Week4_TDD_4B?branch=master)
---

## Authors
```
Part 1:
Driver: Siddhesh Rane (srane96)
Navigator: Srinidhi Sreenath (SrinidhiSreenath)
@version 1.0
@Copyright 2018 Siddhesh Rane

```

```
Part 2:
Driver: Venkatraman Narayanan (vijay4313)
Navigator: Mayank Pathak (mayankpathak10)
@version 2.0
@Copyright 2018 Venkatraman Narayanan

```
## Overview
A simple illustration of pair programming concepts and implementation of PID controller usinf:
* cmake
* googletest
* Travis CI
* Coveralls

## Design review discussions and changes
The following suggestions/changes were made based on a design review meeting:

1. The initial setup considered the time step parameter to be ```const double```, thus sealing the ability to change its value. It was changed to ```double``` for versatile execution of the controller.

2. The original design did not accomodate member-functions that alter/retrieve class parameters/state variables such as, Kp, Kd, Ki and Outputs. New member-functions were added to set and retrieve class parameters

3. The initial test cases were wrong. The incorrect test cases were changed and new test cases were added to increase coverage to 100%

4. Few deviations in commenting styles were corrected to follow Google Style Guide convention

## Standard install via command-line
```
git clone --recursive https://github.com/vijay4313/Week4_TDD_4B
cd <path to repository>
mkdir build
cd build
cmake ..
make
Run tests: ./test/cpp-test
Run program: ./app/pid-controller
```

## Working with Eclipse IDE ##

## Installation

In your Eclipse workspace directory (or create a new one), checkout the repo (and submodules)
```
mkdir -p ~/workspace
cd ~/workspace
git clone --recursive https://github.com/vijay4313/Week4_TDD_4B
```

In your work directory, use cmake to create an Eclipse project for an [out-of-source build] of cpp-boilerplate

```
cd ~/workspace
mkdir -p boilerplate-eclipse
cd boilerplate-eclipse
cmake -G "Eclipse CDT4 - Unix Makefiles" -D CMAKE_BUILD_TYPE=Debug -D CMAKE_ECLIPSE_VERSION=4.7.0 -D CMAKE_CXX_COMPILER_ARG1=-std=c++14 ../Week4_TDD_4B/
```

## Import

Open Eclipse, go to File -> Import -> General -> Existing Projects into Workspace -> 
Select "boilerplate-eclipse" directory created previously as root directory -> Finish

# Edit

Source files may be edited under the "[Source Directory]" label in the Project Explorer.


## Build

To build the project, in Eclipse, unfold boilerplate-eclipse project in Project Explorer,
unfold Build Targets, double click on "all" to build all projects.

## Run

1. In Eclipse, right click on the boilerplate-eclipse in Project Explorer,
select Run As -> Local C/C++ Application

2. Choose the binaries to run (pid-controller, cpp-test for unit testing)


## Debug


1. Set breakpoint in source file (i.e. double click in the left margin on the line you want 
the program to break).

2. In Eclipse, right click on the boilerplate-eclipse in Project Explorer, select Debug As -> 
Local C/C++ Application, choose the binaries to run.

3. If prompt to "Confirm Perspective Switch", select yes.

4. Program will break at the breakpoint you set.

5. Press Step Into (F5), Step Over (F6), Step Return (F7) to step/debug your program.

6. Right click on the variable in editor to add watch expression to watch the variable in 
debugger window.

7. Press Terminate icon to terminate debugging and press C/C++ icon to switch back to C/C++ 
perspetive view (or Windows->Perspective->Open Perspective->C/C++).


## Plugins

- CppChEclipse

    To install and run cppcheck in Eclipse

    1. In Eclipse, go to Window -> Preferences -> C/C++ -> cppcheclipse.
    Set cppcheck binary path to "/usr/bin/cppcheck".

    2. To run CPPCheck on a project, right click on the project name in the Project Explorer 
    and choose cppcheck -> Run cppcheck.


- Google C++ Sytle

    To include and use Google C++ Style formatter in Eclipse

    1. In Eclipse, go to Window -> Preferences -> C/C++ -> Code Style -> Formatter. 
    Import [eclipse-cpp-google-style][reference-id-for-eclipse-cpp-google-style] and apply.

    2. To use Google C++ style formatter, right click on the source code or folder in 
    Project Explorer and choose Source -> Format

[reference-id-for-eclipse-cpp-google-style]: https://raw.githubusercontent.com/google/styleguide/gh-pages/eclipse-cpp-google-style.xml

