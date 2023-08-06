set(LIBHELLO_SRC hello.cpp)
# # include_directories(lib)

# 建立共享库libhello.so
add_library(
    hello  # libname
    SHARED  # shared|static|module
    ${LIBHELLO_SRC}  # source1 source2 ... sourceN
)

# # 建立静态库libhello_static.a
# add_library(
#     hello_static  # libname
#     STATIC  # shared|static|module
#     hello.cpp # source1 source2 ... sourceN
# )

# #可以使共享库和静态库同名
# set_target_properties(
#     hello_static
#     PROPERTIES
#     OUTPUT_NAME
#     "hello"
# )
#SET(LIBRARY_OUTPUT_PATH <路径>) 来指定libhello.so生成位置