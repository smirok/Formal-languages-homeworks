cmake_minimum_required(VERSION 3.16)
project(parserBenchmark)

set(CMAKE_ARGS "${CMAKE_ARGS} -DBENCHMARK_ENABLE_GTEST_TESTS=OFF")

set(CMAKE_CXX_STANDARD 17)

include_directories(../include)
add_subdirectory(benchmark)

add_executable(parserBenchmark
        ../src/parser.cpp ../include/parser.h
        ../src/lexer.cpp ../include/lexer.h
        ../src/reader.cpp ../include/reader.h benchmarks.cpp)

target_link_libraries(parserBenchmark benchmark::benchmark)
