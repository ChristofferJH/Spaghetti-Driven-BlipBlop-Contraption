cmake_minimum_required (VERSION 3.8)



set(EDITOR_NAME "Spaghetti-Driven-BlipBlop-Contraption-EDITOR")

file(GLOB_RECURSE EDITOR_SOURCE_FILES "src/*.cpp")

add_executable(${EDITOR_NAME} ${EDITOR_SOURCE_FILES})

target_include_directories(${EDITOR_NAME} PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")

target_link_libraries(${EDITOR_NAME} PRIVATE ${CORE_NAME})