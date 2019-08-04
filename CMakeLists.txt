cmake_minimum_required(VERSION 3.14)
project(OpenGL-examples)

LINK_DIRECTORIES( ${CMAKE_SOURCE_DIR}/lib )

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

find_package(OpenGL REQUIRED)


include_directories( include )
include_directories(lib/glfw/include)

add_subdirectory(lib/glfw)

set(CMAKE_CXX_STANDARD 14)

add_executable(Testing_OpenGL main.cpp)