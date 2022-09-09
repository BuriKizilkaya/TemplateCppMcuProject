cmake_minimum_required(VERSION 3.15)
project(platform LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(${PROJECT_NAME} STATIC
    Platform.cpp
)

add_library(Bk::Platform ALIAS ${PROJECT_NAME})

target_include_directories(${PROJECT_NAME} PUBLIC .)