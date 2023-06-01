cmake_minimum_required(VERSION 3.6)

project(luac)

include_directories(.)

# 将当前所有源文件保存到 ALL_SRC 变量中
aux_source_directory(. ALL_SRC)
list(REMOVE_ITEM ALL_SRC lua.c luac.c)

add_library(lua ${ALL_SRC})

# 编译 Lua 解释器
add_executable(luac lua.c)
target_link_libraries(luac lua)