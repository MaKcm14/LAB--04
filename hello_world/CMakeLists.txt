cmake_minimum_required(VERSION 3.25.1 FATAL_ERROR)

project(hello_world)

add_library(formatter_ex_lib STATIC ../formatter_ex_lib/code/formatter_ex.cpp ../formatter_ex_lib/code/formatter_ex.h)

add_executable(hello_world ./hello_world.cpp)

target_link_libraries(hello_world formatter_ex_lib)
