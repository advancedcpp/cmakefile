#Minimum required version of CMake
cmake_minimum_required(VERSION 3.0)

# Project name and version
project(MyProject VERSION 1.0)

# Add executable target
add_executable(my_executable main.cpp hello.cpp)

# Optionally, set C++ standard (e.g., C++11, C++14, C++17)
# Set include directories for headers
target_include_directories(my_executable PRIVATE
    ${CMAKE_SOURCE_DIR}/include
)
set_target_properties(my_executable PROPERTIES
    CXX_STANDARD 11
    CXX_STANDARD_REQUIRED YES
    CXX_EXTENSIONS NO
)