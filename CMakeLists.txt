cmake_minimum_required(VERSION 3.22 FATAL_ERROR)
set(PROJECT_NAME city)
project(${PROJECT_NAME})


SET (PROJECT_SOURCE_DIR "${PROJECT_SOURCE_DIR}/src")

add_executable(${PROJECT_NAME} ${PROJECT_SOURCE_DIR}/main.cpp)

SET(BUILD_SHARED_LIBS OFF CACHE BOOL "" FORCE)
SET(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
SET(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
SET(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
SET(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${PROJECT_NAME} glfw)

add_subdirectory(external/glad)
target_link_libraries(${PROJECT_NAME} glad)