cmake_minimum_required(VERSION 3.10) #最低cmake版本要求
project(project) #项目名
set(CMAKE_CXX_STANDARD 11) #使用c++11标准


#生成的【.a .so文件】、【可执行文件】、【exe都放在bin文件夹】
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin) 
#所有.cpp源文件 存到变量SRC_LIST
aux_source_directory(src SRC_LIST)
# 指定头文件路径
include_directories(include)  



# 添加可执行文件
add_executable(project ${SRC_LIST})