# Create a new 'target' called simplelib (not to be confused with the directory name) which is
# a static library. By listing the header file as a source file, if it changes, CMake will know
# that the target needs to be recompiled.
add_library(simplelib STATIC src/simplelib.cpp src/simplelib.hpp)
