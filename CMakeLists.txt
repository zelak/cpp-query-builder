cmake_minimum_required(VERSION 2.8)
project(cpp_query_builder)

# set external dependencies path
set(EXTERNAL_PATH "vendor")

# download catch C++ unit test framework
set(CATCH_PATH "${EXTERNAL_PATH}/philsquared/catch/catch.hpp")
set(CATCH_GIT_URL "https://raw.githubusercontent.com/philsquared/Catch/master/single_include/catch.hpp")
if (NOT EXISTS "${CATCH_PATH}")
    file(DOWNLOAD "${CATCH_GIT_URL}" "${CATCH_PATH}")
endif()

# set compile flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++0x")

# source files
set(SOURCE_FILES
    test/test_main.cpp)

add_executable(cpp_query_builder ${SOURCE_FILES})