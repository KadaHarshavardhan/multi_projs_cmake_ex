# Compile multiple C projects using CMAKE

## Descpription
This is a basic example which shows how to compile multiple projects and generate multiple Binaries for each project.

Here, are two projects **proj1** and **proj2** which are indivual projects, shown below

```
./
├── CMakeLists.txt
├── proj1
│   ├── CMakeLists.txt
│   ├── inc
│   │   ├── cal.h
│   │   └── CMakeLists.txt
│   └── src
│       ├── add.c
│       ├── CMakeLists.txt
│       └── main.c
├── proj2
│   ├── CMakeLists.txt
│   ├── inc
│   │   ├── cal.h
│   │   └── CMakeLists.txt
│   └── src
│       ├── add.c
│       ├── CMakeLists.txt
│       └── main.c
└── README.md


```
After the projects are built, we get a */bin* directories created which containes the executable for each project

## Build

Step 1: clone the project using,

` git clone  https://github.com/KadaHarshavardhan/multi_projs_cmake_ex`

Step 2: Enter this directory 

    cd multi_projs_cmake_ex

Step 3: Create a **cmake** directory where all the build files and executables are present

    mkdir cmake
    cd cmake

Step 4: Buid the projects
    
    cmake ..
    make
This will build the projects

## Test

In the **cmake** directory, there is a **bin** created for each project which contains executable

BIN Directories: `multi_projs_cmake_ex/cmake/proj1/bin` , `multi_projs_cmake_ex/cmake/proj2/bin`  
Execute using: `./proj1` or `./proj2`

## Collapse
Remove all the build files, 
    
    make clean
    rm -rf cmake

NOTE: For rebuilding the projects, follow the **Build** section steps.