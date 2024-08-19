add_library(project-cpp-core OBJECT)
add_library(project-cpp::core ALIAS project-cpp-core)

target_sources(project-cpp-core PRIVATE
  foo.h
)

target_include_directories(project-cpp-core
  PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:include>
)

add_executable(project-cpp)

target_sources(project-cpp PRIVATE
  main.cpp
)

# Link library dependencies
target_link_libraries(project-cpp PRIVATE
  compiler_flags
  project-cpp-core
)
