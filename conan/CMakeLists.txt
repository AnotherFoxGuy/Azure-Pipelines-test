cmake_minimum_required(VERSION 3.10)
project(TestProject)

include(../pmm.cmake)
pmm(CONAN DEBUG)

add_executable(dummy main.cpp)
target_link_libraries(dummy PRIVATE CONAN_PKG::Catch2)

add_test(dummy dummy)
