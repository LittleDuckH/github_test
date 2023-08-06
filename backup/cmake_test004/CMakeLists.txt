cmake_minimum_required(VERSION 3.16)
PROJECT(HELLOLIB)
#用于查找lib下的hello.hpp文件
include_directories(lib)

# aux_source_directory()

# 指定libhello.so生成位置
add_subdirectory(lib build_lib)
add_subdirectory(src)
# add_executable(main main.cpp)

# target_link_libraries(main PRIVATE hello_static)# 链接定义动态库,不连接会出现函数未定义的情况
