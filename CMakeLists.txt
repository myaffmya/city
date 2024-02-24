cmake_minimum_required(VERSION 3.22 FATAL_ERROR)
project(city)

SET (PROJECT_SOURCE_DIR "${PROJECT_SOURCE_DIR}/src")

add_executable(city ${PROJECT_SOURCE_DIR}/main.cpp)