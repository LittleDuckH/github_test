include_directories(../lib)
add_executable(main main.cpp)
# # 建立共享库libhello.so
# add_library(
#     hello  # libname
#     SHARED  # shared|static|module
#     ../lib/hello.cpp  # source1 source2 ... sourceN
# )


target_link_libraries(main hello)# 链接定义动态库,不连接会出现函数未定义的情况
~