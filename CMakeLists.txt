cmake_minimum_required(VERSION 3.10)
project(BasicCppProgram)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add Google Test
enable_testing()
find_package(GTest REQUIRED)

# Main executable
add_executable(BasicCppProgram main.cpp math_operations.cpp)

# Unit tests executable
add_executable(unit_tests tests/unit_tests.cpp math_operations.cpp)
target_link_libraries(unit_tests GTest::gtest GTest::gtest_main)

# Register tests
add_test(NAME MathOperationsTest COMMAND unit_tests)