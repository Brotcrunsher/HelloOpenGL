cmake_minimum_required(VERSION 3.13.3 FATAL_ERROR)

project(HelloOpenGL C CXX)
add_executable(HelloOpenGL HelloOpenGL.cpp)

add_subdirectory(glew-2.1.0/build/cmake)
include_directories(glew-2.1.0/include)
target_link_libraries(HelloOpenGL glew_s)

add_subdirectory(glfw-3.3.2)
include_directories(glfw-3.3.2/include)
target_link_libraries(HelloOpenGL glfw ${GLFW_LIBRARIES})
