if (BUILD_SHARED_LIBS)
    add_library(greetings SHARED
        hello.cpp
        good_morning.cpp
        )
else()
    add_library(greetings STATIC
        hello.cpp
        good_morning.cpp
        )
endif()
