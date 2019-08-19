cmake_minimum_required(VERSION 3.10)
project(TestProject)

include(../pmm.cmake)
pmm(VCPKG
    REVISION 2019.07
    REQUIRES catch2
    DEBUG
    )

find_package(Catch2 CONFIG REQUIRED)

add_executable(dummy main.cpp)
target_link_libraries(dummy PRIVATE Catch2::Catch2)
