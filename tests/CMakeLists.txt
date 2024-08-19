include(GoogleTest)

find_package(GTest CONFIG REQUIRED)

enable_testing()

add_executable(project-test)

target_sources(project-test
  PRIVATE
    foo.test.cpp
    main.cpp
)

target_link_libraries(project-test
  PRIVATE
    compiler_flags
    GTest::gtest
    GTest::gtest_main
    project-cpp::core
)

gtest_discover_tests(project-test)
