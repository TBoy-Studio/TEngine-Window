cmake_minimum_required(VERSION 3.10)

project(tengine-window VERSION 1.0)

# C11 is also fine
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED True)

# Used by clang language server for code completion
set(CMAKE_EXPORT_COMPILE_COMMANDS True)

# Build as static lib
set(BUILD_SHARED_LIBS False)

# Build with all warnings enabled and optimize maximally, this is the default behaviour
add_compile_options(-Wall -Wextra -Wpedantic -O3)

# Include directories for header files
include_directories(${PROJECT_SOURCE_DIR}/include)

add_library( ${PROJECT_NAME} ${PROJECT_SOURCE_DIR}/src/window.c )