cmake_minimum_required(VERSION 3.10)

set(MAIN_TARGET "draugr")
set(SRCS main.cpp)
add_subdirectory(src)

add_compile_options(
        -std=c++17
        -Werror
        -Wall
        -Wextra
        -Wpedantic
        -Wno-unused-parameter
)

project(${MAIN_TARGET})

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/..")

add_executable(${MAIN_TARGET} ${SRCS})

target_link_libraries(${MAIN_TARGET} PUBLIC src)

target_include_directories(${MAIN_TARGET} PUBLIC
        "${PROJECT_BINARY_DIR}"
        "${PROJECT_SOURCE_DIR}/src"
        )