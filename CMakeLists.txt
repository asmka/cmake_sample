cmake_minimum_required(VERSION 3.16)
project(CMAKE_SAMPLE VERSION 1.0.0)

include_directories(AFTER
    ${PROJECT_SOURCE_DIR}/include
    )

# -std=c++17
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_compile_options(-Wall
    $<$<CONFIG:Release>:"SHELL: -O3">             # Release
    $<$<CONFIG:Debug>:"SHELL: -O0 -g">            # Debug
    $<$<CONFIG:RelWithDebgInfo>:"SHELL: -O3 -g">  # RelWithDebInfo
    )

add_compile_definitions(
    $<$<NOT:$<CONFIG:Debug>>:NDEBUG>     # Except for Debug
    )

add_subdirectory(src)
