cmake_minimum_required(VERSION 3.10)
project(TestProject)

include(../pmm.cmake)
pmm(VCPKG
    REVISION 2019.07
    REQUIRES catch2
    DEBUG
    )

find_package(catch2 REQUIRED CONFIG)

add_executable(dummy main.cpp)
target_link_libraries(dummy PRIVATE catch2::catch2)
