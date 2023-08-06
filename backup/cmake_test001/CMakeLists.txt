# # cmake_minimum_required(VERSION 3.10.2)
# # set(CMAKE_EXPORT_COMPILE_COMMANDS TRUE)

PROJECT(HELLO)
SET(SRC_LIST main.cpp)
# MESSAGE(STATUS "This is Binary dir" ${HELLO_BINARY_DIR})
# MESSAGE(STATUS "This is SOURCE dir" ${HELLO_SOURCE_DIR})
MESSAGE(STATUS "This is Binary dir " ${PROJECT_BINARY_DIR})
MESSAGE(STATUS "This is SOURCE dir " ${PROJECT_SOURCE_DIR})
ADD_EXECUTABLE(hello ${SRC_LIST})
# # add_executable(t1 t1.cpp)

# # 简易版
# project(MA)
# add_executable(ma main.cpp)