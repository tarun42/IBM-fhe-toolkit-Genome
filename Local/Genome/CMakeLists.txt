cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

# Use -std=c++14 as default.
set(CMAKE_CXX_STANDARD 14)
# Disable C++ extensions
set(CMAKE_CXX_EXTENSIONS OFF)
# Require full C++ standard
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(BGV_binary_arithmetic LANGUAGES CXX)

find_package(helib 1.0.0 EXACT REQUIRED)

add_executable(Genome Genome.cpp)

target_link_libraries(Genome helib)
