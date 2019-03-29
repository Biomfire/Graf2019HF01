cmake_minimum_required(VERSION 3.5)
project(grafhazi)

set(SOURCE_FILES Skeleton.cpp framework.cpp framework.h)
set(CMAKE_CXX_STANDARD 11)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(GLEW REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS} ${GLEW_INCLUDE_DIRS})

link_libraries(${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${GLEW_LIBRARIES})

add_executable(grafhazi ${SOURCE_FILES})
