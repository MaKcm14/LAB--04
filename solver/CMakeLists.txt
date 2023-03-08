cmake_minimum_required(VERSION 3.25.1 FATAL_ERROR)

project(solver)

add_library(formatter_ex_lib STATIC ../formatter_ex_lib/code/formatter_ex.cpp ../formatter_ex_lib/code/formatter_ex.h)

add_library(solver_lib STATIC ../solver_lib/code/solver.h ../solver_lib/code/solver.cpp)

add_executable(solver ./equation.cpp)

target_link_libraries(solver formatter_ex_lib solver_lib)
