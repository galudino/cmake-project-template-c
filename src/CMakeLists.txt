cmake_minimum_required(VERSION "3.18")
project("cmake-project-template-c-library")

set(C_STANDARD "11") # C11
set(CFLAGS "-Wall -Werror -pedantic-errors")

set(CMAKE_C_STANDARD ${C_STANDARD})
set(CMAKE_C_FLAGS ${CMAKE_C_FLAGS} ${CFLAGS})

add_library("cmake-project-template-c-library" "header.h" "source.c")
target_include_directories("cmake-project-template-c-library" PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
