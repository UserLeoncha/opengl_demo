file(GLOB src *.cpp)
add_executable(demo ${src})

target_link_libraries(demo glfw)
target_link_libraries(demo glad)
target_link_libraries(demo stb)
target_link_libraries(demo glm)
