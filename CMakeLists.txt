cmake_minimum_required(VERSION 3.5)

set(PROJECT_NAME "libtvlm")

project(${PROJECT_NAME})
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
file(GLOB_RECURSE SRC "*.cpp" "*.h")
add_library(${PROJECT_NAME} ${SRC})

set(TINY_LIBRARIES "${TINY_LIBRARIES};${PROJECT_NAME}" PARENT_SCOPE)
set(TINY_INCLUDES "${TINY_INCLUDES};${CMAKE_CURRENT_SOURCE_DIR}" PARENT_SCOPE)