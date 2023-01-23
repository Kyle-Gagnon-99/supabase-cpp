# Specify the minimum version for CMake
cmake_minimum_required(VERSION 3.16)

# Set the project name 
set(VERSION_MAJOR 1)
set(VERSION_MINOR 0)
project(SupabaseCpp 
    VERSION ${VERSION_MAJOR}.${VERSION_MINOR} 
    DESCRIPTION "A C++ binding for Supabase"
    LANGUAGES CXX)
message(STATUS "Build supabasecpp: ${PROJECT_VERSION}")

if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "Debug")
endif()

set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake" ${CMAKE_MODULE_PATH})

add_subdirectory("src/")
add_subdirectory("docs/")
add_subdirectory("tests/")