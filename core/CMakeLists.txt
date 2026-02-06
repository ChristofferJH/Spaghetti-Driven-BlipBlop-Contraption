cmake_minimum_required (VERSION 3.8)

add_subdirectory ("lib")

file(GLOB_RECURSE CORE_SOURCE_FILES "src/*.cpp")

add_library(${CORE_NAME} STATIC ${CORE_SOURCE_FILES})

target_include_directories("${CORE_NAME}" PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")

target_link_libraries(${CORE_NAME} PUBLIC glfw openGL32)
target_include_directories("${CORE_NAME}" PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/lib/glfw/include")