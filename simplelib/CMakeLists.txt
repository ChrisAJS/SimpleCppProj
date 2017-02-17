# Create a new 'target' called simplelib (not to be confused with the directory name) which is
# a static library. By listing the header file as a source file, if it changes, CMake will know
# that the target needs to be recompiled.
add_library(simplelib STATIC src/simplelib.cpp src/simplelib.hpp)

# Use find_package to Locate CppUTest; this will populate _some_ variables
# which will be used to define include directories and linker directories 
# and library names
find_package(CppUTest)

# One approach to adding unit tests is to create an
# executable for each test suite
add_executable(first_test test/first_test.cpp)

# ${CppUTest_...} variables are defined by the find_package invocation
target_include_directories(first_test PRIVATE ${CppUTest_INCLUDE_DIRS})
target_link_libraries(first_test ${CppUTest_LIBRARIES})