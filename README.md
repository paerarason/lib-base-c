# C Library Boilerplate

A basic boilerplate for creating a C library using CMake. This repository provides a simple starting point to build and distribute your own C library.

## Project Structure

- `include/`: Public header files for the library.
- `src/`: Source files for the library.
- `example/`: Example application linking against the library.
- `CMakeLists.txt`: CMake build configuration.

## Requirements

- CMake (version 3.10 or higher)
- A C compiler (GCC, Clang, MSVC, etc.)

## Building the Project

Create a build directory, run CMake to configure, and then build the project:

```bash
mkdir build
cd build
cmake ..
cmake --build .
```

## Running the Example

After building, you can run the example executable from the build directory:

```bash
./example_app
```

## Getting Started with Your Library

1. Rename `mylib` in `CMakeLists.txt`, `src/mylib.c`, and `include/mylib.h` to your desired library name.
2. Add your functions to the header and source files.
3. Update `example/main.c` to test your new functions.
