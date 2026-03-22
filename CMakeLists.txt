cmake_minimum_required(VERSION 3.10)
project(lib_base_c VERSION 1.0.0 LANGUAGES C)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Define the library
add_library(mylib src/mylib.c)

# Specify include directories for the library
target_include_directories(mylib PUBLIC 
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)

# Example executable
add_executable(example_app example/main.c)
target_link_libraries(example_app PRIVATE mylib)
