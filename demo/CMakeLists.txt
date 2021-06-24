cmake_minimum_required(VERSION "3.18")
project("cmake-project-template-c-demo")

set(C_STANDARD "11")
set(CFLAGS "-Wall -Werror -pedantic-errors")

set(CMAKE_C_STANDARD ${C_STANDARD})
set(CMAKE_C_FLAGS ${CMAKE_C_FLAGS} ${CFLAGS})

add_executable("demo" "main.c")
target_link_libraries("demo" LINK_PUBLIC "cmake-project-template-c-library")
