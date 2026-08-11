cmake_minimum_required(VERSION 3.10)
project(slimstack C)

set(CMAKE_C_STANDARD 11)

# Enable strict warnings
if(CMAKE_C_COMPILER_ID STREQUAL "GNU" OR CMAKE_C_COMPILER_ID STREQUAL "Clang")
    add_compile_options(-Wall -Wextra -Wpedantic -Werror)
endif()

# Where to find headers
include_directories(include)

# What to build
add_executable(slimstack
    src/*
)

target_link_libraries(slimstack m)
