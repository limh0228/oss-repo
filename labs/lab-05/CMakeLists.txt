cmake_minimum_required(VERSION 3.0)
project(Block C)

add_library(staticlib source/block.c)
add_library(dynlib SHARED source/block.c)

add_executable(static_block program.c)
add_executable(dynamic_block program.c)

target_link_libraries(static_block staticlib)
target_link_libraries(dynamic_block dynlib)