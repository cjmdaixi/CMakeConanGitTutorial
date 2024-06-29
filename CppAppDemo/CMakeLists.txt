cmake_minimum_required(VERSION 3.28)
project(CppAppDemo VERSION 0.1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(LibDemo REQUIRED CONFIG)

add_executable(CppAppDemo main.cpp)

target_link_libraries(CppAppDemo PRIVATE LibDemo)