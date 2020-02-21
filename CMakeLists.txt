cmake_minimum_required(VERSION 3.16)
project(cmake_sample VERSION 1.0)

add_subdirectory(src)

#set(CMAKE_CXX_STANDARD 17)
#set(CMAKE_CXX_STANDARD_REQUIRED True)
target_compile_options(cmake_sample PUBLIC -Wall)
target_compile_features(cmake_sample PUBLIC cxx_std_17)
target_compile_options(cmake_sample PUBLIC
    $<$<CONFIG:Release>:-O3>             # Release
    $<$<CONFIG:Debug>:-O0 -g>            # Debug
    $<$<CONFIG:RelWithDebgInfo>:-O3 -g>  # RelWithDebInfo
    )
target_compile_definitions(a.out PUBLIC
    $<$<NOT:$<CONFIG:Debug>>:NDEBUG>     # Debug以外
    )
