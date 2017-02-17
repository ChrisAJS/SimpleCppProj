# Create an executable 'target' called app (not to be confused with the directory name)
add_executable(app src/main.cpp)

# Define libraries that must be linked to the app target
# As simplelib is in the project, it will be resolved
target_link_libraries(app simplelib)
