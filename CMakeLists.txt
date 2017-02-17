# Set minimum required CMake version to appease CMake
cmake_minimum_required(VERSION 3.0)

# Calling project will initialise some useful variables
# Such as: 
#   PROJECT_NAME (SimpleCppProj)
#   PROJECT_VERSION_MAJOR (0)
#   PROJECT_VERSION_MINOR (0)
#   PROJECT_VERSION_PATCH (0)
project(SimpleCppProj VERSION 0.0.0 LANGUAGES CXX)

# Add application and library to the project
add_subdirectory(app) 		# 'app' references directory name
add_subdirectory(simplelib) # 'simplelib' references directory name

add_dependencies(app simplelib) # In this instance 'app' and 'simplelib' are both _targets_, not directories

# Add unit tests here to expose unit tests to build systems

# Enable CTest
enable_testing()

# A test suite can be given a name (FirstTest)
# and then a command to execute (first_test)
add_test(FirstTest simplelib/first_test)