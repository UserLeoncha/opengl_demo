cmake_minimum_required(VERSION 3.10)
project(demo)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD_REQUIRED true)
set(CMAKE_EXPORT_COMPILECOMMANDS ON)

set(R ${CMAKE_SOURCE_DIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${R}/output)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${R}/libs)
include_directories(${R}/thirdparty)
add_subdirectory(thirdparty)
add_subdirectory(src)
file(GLOB_RECURSE RESOURCE_FILES "resources/**/*")
install(DIRECTORY resources/
        DESTINATION ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/resources
)