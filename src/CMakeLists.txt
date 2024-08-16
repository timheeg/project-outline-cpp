add_executable(project-cpp)

target_include_directories(project-cpp
  PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:include>
)

target_sources(project-cpp PRIVATE
  main.cpp
)
