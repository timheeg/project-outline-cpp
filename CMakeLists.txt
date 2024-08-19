cmake_minimum_required(VERSION 3.29)

project(project-cpp LANGUAGES CXX)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

include(compiler_flags)

add_subdirectory(src)
add_subdirectory(tests)
