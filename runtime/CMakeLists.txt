cmake_minimum_required (VERSION 3.8)



set(RUNTIME_NAME "Spaghetti-Driven-BlipBlop-Contraption-RUNTIME")

file(GLOB_RECURSE RUNTIME_SOURCE_FILES "src/*.cpp")

add_executable(${RUNTIME_NAME} ${RUNTIME_SOURCE_FILES})

target_include_directories(${RUNTIME_NAME} PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")

target_link_libraries(${RUNTIME_NAME} PRIVATE ${CORE_NAME})