cmake_minimum_required(VERSION 2.8)

SET(CMAKE_COLOR_MAKEFILE ON)
if(${USE_CLANG})
    SET (CMAKE_CXX_COMPILER  "clang++")
endif()

set(CMAKE_CXX_FLAGS "-pthread -Wall -fno-strict-aliasing --std=c++0x")
set(CMAKE_CXX_FLAGS_DEBUG "-g -ggdb -O0")
set(CMAKE_CXX_FLAGS_RELEASE "-O3 -pipe")


# Adding bins
add_executable(functors_example functors_example.cpp)
target_link_libraries (functors_example) 

