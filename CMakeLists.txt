# CMakeLists.txt for basic C++ program

cmake_minimum_required(VERSION 3.10)
project(BasicCppProgram)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(BasicCppProgram main.cpp)