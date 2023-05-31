cmake_minimum_required(VERSION 3.0.0)
project(PILua4 VERSION 0.1.0)

add_subdirectory(./lib/lua)
include_directories(./lib/lua)

add_executable(PILua4 main.c)
target_link_libraries(PILua4 lua)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
