# CMake Minimum Required Version Information
cmake_minimum_required(VERSION 3.10)

# Display Make Log
set(CMAKE_VERBOSE_MAKEFILE ON)

project(
    # Project Name
    Solution
)

# Release Mode Build Options
set(CMAKE_C_FLAGS_RELEASE_INIT     "-O2")
set(CMAKE_CXX_FLAGS_RELEASE_INIT   "-O2")

# Debug Mode Build Options
set(CMAKE_C_FLAGS_DEBUG_INIT     "-g -DDEBUG")
set(CMAKE_CXX_FLAGS_DEBUG_INIT   "-g -DDEBUG")

# Change Default Build Result Path
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY          ${PROJECT_BINARY_DIR}/release/bin) 
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY          ${PROJECT_BINARY_DIR}/release/lib) 

# Jump To Sub Directories
add_subdirectory(source/lib)
add_subdirectory(source/exe)
