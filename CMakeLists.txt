cmake_minimum_required(VERSION 2.8)
project(alloc)

include_directories(
        alloc/
)


file( GLOB_RECURSE
        SOURCES
        alloc/*.cpp

        alloc/*.h
)

set(alloc_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR} PARENT_SCOPE)

add_library(alloc ${SOURCES})

target_link_libraries(alloc)