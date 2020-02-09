cmake_minimum_required(VERSION 3.0)
project(CSV++_test LANGUAGES CXX VERSION 0.0.1)

find_package(Catch2 REQUIRED)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include_directories(include/)
add_executable(csvpp_test test/main.cpp)
target_link_libraries(csvpp_test Catch2::Catch2)

include(CTest)
include(Catch)
catch_discover_tests(csvpp_test WORKING_DIRECTORY test/)
