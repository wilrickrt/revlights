cmake_minimum_required(VERSION 3.21)

set(revlights_VERSION 0.1.0)

project(revlights
        VERSION ${revlights_VERSION}
        DESCRIPTION "Assetto Corsa Competizione rev lights"
        HOMEPAGE_URL "https://github.com/wilrickrt/revlights"
        LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)

## Static builds on Windows
if (MSVC)
    set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")
endif()

include_directories(include)
add_subdirectory(src)
