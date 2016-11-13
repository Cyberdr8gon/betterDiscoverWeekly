cmake_minimum_required (VERSION 2.6)
project ( hashedGraphLib )

set(CMAKE_CXX_FLAGS "-g -Wall -std=c++14")

add_executable( test hashedgraph_test.cpp hashedgraph.cpp )
target_link_libraries( test gtest gtest_main pthread )
