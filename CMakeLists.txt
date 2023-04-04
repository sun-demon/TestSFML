cmake_minimum_required(VERSION 3.8)

project(TestSFML VERSION 0.1)

find_package(SFML COMPONENTS graphics REQUIRED)

add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(${PROJECT_NAME} sfml-graphics)
