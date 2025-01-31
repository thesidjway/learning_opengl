cmake_minimum_required(VERSION 3.17)
project(graphics)

set(CMAKE_CXX_STANDARD 14)

find_package(GLEW REQUIRED)
find_package(glfw3 3.2 REQUIRED)

include_directories(${GLEW_INCLUDE_DIRS} include/GLM)

add_executable(Init src/Init.cpp)
target_link_libraries(Init ${GLEW_LIBRARIES} glfw GL)

add_executable(Shaders src/Shaders.cpp)
target_link_libraries(Shaders ${GLEW_LIBRARIES} glfw GL)

add_executable(UniformVariable src/UniformVariable.cpp)
target_link_libraries(UniformVariable ${GLEW_LIBRARIES} glfw GL)

add_executable(Transformations src/Transformations.cpp)
target_link_libraries(Transformations ${GLEW_LIBRARIES} glfw GL)