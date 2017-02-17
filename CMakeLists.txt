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

add_subdirectory(app)
add_subdirectory(simplelib)
