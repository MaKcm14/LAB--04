cmake_minimum_required(VERSION 3.25.1 FATAL_ERROR)

project(new_ex_formatter)

add_library(formatter_lib STATIC ../formatter_lib/code/formatter.cpp ../formatter_lib/code/formatter.h)

add_executable(formatter_ex ./code/formatter_ex.cpp ./code/formatter_ex.h)

target_link_libraries(formatter_ex formatter_lib)
