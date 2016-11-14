cmake_minimum_required (VERSION 2.6)
project ( cpplibs )

set(CMAKE_CXX_FLAGS "-g -Wall -std=c++14")

include_directories(include)

set(HEADER_FILES include/abstractmusicdata.h include/hashedgraph.h )
set(SOURCES src/hashedgraph_test.cpp src/hashedgraph.cpp src/abstractmusicdata.cpp )

add_executable( testexe ${SOURCES} )
target_link_libraries( testexe gtest gtest_main pthread )
