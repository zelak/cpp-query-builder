cmake_minimum_required(VERSION 3.0)
project(cpp_query_builder)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES test/test_main.cc)
add_executable(cpp_query_builder ${SOURCE_FILES})
