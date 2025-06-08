cmake_minimum_required(VERSION 3.15)
project(OpenGLApp)

set(CMAKE_CXX_STANDARD 17)

# Conan will set CMAKE_PREFIX_PATH via toolchain, so just find_package
find_package(glfw3 REQUIRED)
find_package(glad REQUIRED)

add_executable(OpenGLApp src/main.cpp)

target_link_libraries(OpenGLApp
    glfw
    glad::glad
)


if(APPLE)
    target_link_libraries(OpenGLApp "-framework OpenGL")
endif()
