cmake_minimum_required(VERSION 3.17)
project(graphics)

set(CMAKE_CXX_STANDARD 14)

find_package(GLEW REQUIRED)
find_package(glfw3 3.2 REQUIRED)

include_directories(${GLEW_INCLUDE_DIRS})

add_executable(Init src/Init.cpp)
target_link_libraries(Init ${GLEW_LIBRARIES} glfw GL)