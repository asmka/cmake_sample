add_subdirectory(greetings)

add_executable(cmake_sample main.cpp)
if (BUILD_SHARED_LIBS)
    target_link_libraries(cmake_sample INTERFACE
        greetings
        )
else()
    target_link_libraries(cmake_sample PRIVATE
        greetings
        )
endif()
