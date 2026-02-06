cmake_minimum_required (VERSION 3.8)



set(CORE_NAME "Spaghetti-Driven-BlipBlop-Contraption-CORE")

file(GLOB_RECURSE CORE_SOURCE_FILES "src/*.cpp")

add_library(${CORE_NAME} STATIC ${CORE_SOURCE_FILES})

target_include_directories("${CORE_NAME}" PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")