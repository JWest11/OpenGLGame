cmake_minimum_required(VERSION 3.0.0)
project(OpenGLGame VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(OpenGLGame main.cpp)

find_package(GLEW REQUIRED)
target_link_libraries(OpenGLGame PRIVATE GLEW::GLEW)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(OpenGLGame PRIVATE glfw)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
