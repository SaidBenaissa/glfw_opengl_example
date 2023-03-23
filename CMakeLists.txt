cmake_minimum_required(VERSION 3.0)
project(my_opengl_program)

# Find OpenGL
find_package(OpenGL REQUIRED)

# Find GLFW
find_package(glfw3 REQUIRED)

# Add your source files
add_executable(my_opengl_program src/main.cpp)

# Link with OpenGL and GLFW
target_link_libraries(my_opengl_program ${OPENGL_LIBRARIES} glfw)

# Specify required C++ features
target_compile_features(my_opengl_program PUBLIC cxx_std_11)

# Include the necessary directories
target_include_directories(my_opengl_program PUBLIC ${OPENGL_INCLUDE_DIRS} ${GLFW_INCLUDE_DIRS})
