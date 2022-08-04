# @file utils/CMakeLists.txt
# @author HinsShum hinsshum@qq.com
# @date 2021/01/06 16:24:03
# @encoding utf-8
# @brief Here's the first line of every CMakeLists.txt,
#        which is the required name of the file CMake looks for:
cmake_minimum_required(VERSION 3.1)

set(TARGET_NAME "utils")
set(G_LIBS ${G_LIBS} ${TARGET_NAME} PARENT_SCOPE)
set(TARGET_INC_VPATH ${CMAKE_CURRENT_SOURCE_DIR}/inc)
file(GLOB_RECURSE TARGET_C_FILES "*.c")

add_library(${TARGET_NAME} STATIC ${TARGET_C_FILES})
target_include_directories(${TARGET_NAME} PUBLIC ${TARGET_INC_VPATH})