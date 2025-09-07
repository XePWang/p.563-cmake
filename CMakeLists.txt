cmake_minimum_required(VERSION 3.10)
project(p563 C)

# 设置 C 标准
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# 查找所有源文件
file(GLOB_RECURSE P563_SOURCES 
    "${CMAKE_CURRENT_SOURCE_DIR}/source/*.c"
)

# 添加头文件目录
include_directories(
    "${CMAKE_CURRENT_SOURCE_DIR}/include"
)

# 定义可执行文件
add_executable(p563 ${P563_SOURCES})

# 链接数学库
target_link_libraries(p563 m)

# 设置输出目录
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)
