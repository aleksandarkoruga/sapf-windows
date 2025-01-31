# Set the minimum required version of CMake
cmake_minimum_required(VERSION 3.10)

# Define the project name and language
project(sapf-windows)

# Set the C++ standard to use
set(CMAKE_CXX_STANDARD 20)

# Add include directory for header files
include_directories(${PROJECT_SOURCE_DIR}/include)

# Collect all the source files in the src folder
file(GLOB SOURCES "${PROJECT_SOURCE_DIR}/src/*.cpp")

# Create a Visual Studio project (you don't need to add an executable target)
add_library(sapf-windows STATIC ${SOURCES})
