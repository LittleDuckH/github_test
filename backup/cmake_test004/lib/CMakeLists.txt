set(LIBHELLO_SRC hello.cpp)
# # include_directories(lib)

# 建立共享库libhello.so
# If 需要提供绝对路径 ${CMAKE_CURRENT_SOURCE_DIR}指当前CMakeLists.txt所在的路径
IF(EXISTS ${CMAKE_CURRENT_SOURCE_DIR})
    add_library(
        hello  # libname
        SHARED  # shared|static|module
        hello.cpp  # source1 source2 ... sourceN
    )
    # 输出 lib 目录的绝对路径
    message(STATUS "Lib directory: ${CMAKE_CURRENT_SOURCE_DIR}")
    message("Hello, World!")
ENDIF()

IF(IS_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/hello.cpp)
    message("lib exist!!!")
ELSE()
    message("lib isexist!!!")
ENDIF()

# 从0到taotal(10)以1为步进
FOREACH(var RANGE 10)
    message(${var})
ENDFOREACH(var)

# FOREACH(loop_var RANGE start stop [step])
# ENDFOREACH(loop_var)
# 从start开始到stop结束，以step为步进、
# 遇到ENDFOREACH指令才能被真正的执行 

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