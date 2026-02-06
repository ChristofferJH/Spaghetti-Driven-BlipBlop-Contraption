cmake_minimum_required (VERSION 3.8)


file(GLOB_RECURSE IMGUI_SOURCE_FILES "*.cpp")

add_library(imgui STATIC ${IMGUI_SOURCE_FILES})

target_link_libraries(imgui PRIVATE glfw openGL32)
target_include_directories(imgui PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")