cmake_minimum_required(VERSION 3.28)
project(CppLibDemo VERSION 0.1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

configure_file(${CMAKE_SOURCE_DIR}/LibDemoConfig.cmake.in LibDemoConfig.cmake @ONLY)

add_library(CppLibDemo STATIC libdemo.h libdemo.cpp)

install(TARGETS CppLibDemo ARCHIVE DESTINATION lib)
install(FILES libdemo.h DESTINATION include)
install(FILES conanfile.py DESTINATION .)
install(FILES ${CMAKE_BINARY_DIR}/LibDemoConfig.cmake DESTINATION lib/cmake)