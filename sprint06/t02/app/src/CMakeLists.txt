cmake_minimum_required(VERSION 3.18.2)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_CXX_EXTENSIONS OFF)

set(CMAKE_CXX_STANDARD_REQUIRED YES)

project(t_00_lib)

add_compile_options(
    -pipe
    -Wall
    -Wextra
    -Werror
    -Wpedantic
)

set(TARGET libsrc)

include_directories(. ../resources)

SET(CMAKE_CXX_STANDARD 17)

SET(CMAKE_CXX_FLAGS "-std=c++17 -Wall -Wextra -Werror -Wpedantic")

add_library(${TARGET} Creatures.cpp Spells.cpp)