cmake_minimum_required(VERSION 3.10)
project(TestProject)

include(../pmm.cmake)
pmm(CMakeCM ROLLING)

include(cotire)

add_executable(dummy-program main.cpp)

cotire(dummy-program)
