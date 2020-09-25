# CMake Minimum Required Version Information
cmake_minimum_required(VERSION 3.10)

project(
    # Project Name
    testlib
)

# Project Compile Defines
#set(DEFINES
#    ${COMMON_DEFINES}
#)

# Project Compile Options
#set(CFLAGS
#    ${COMMON_CFLAGS}
#)

# Compile Include Paths
#set(INCS
#    ${CMAKE_CURRENT_SOURCE_DIR}/Inc
#)

# Compile Source Files
set(SRCS
    lib.cpp
)

# Library Target[ *.lib | *.a | *.dll | *.so  ]
add_library(${PROJECT_NAME} SHARED  ${SRCS})

set_target_properties(${PROJECT_NAME} PROPERTIES VERSION 1.2.3 SOVERSION 1)

# Add Target Compile Definitions
#target_compile_definitions( ${PROJECT_NAME} PRIVATE ${DEFINES})

# Add Target Compile Options
#target_compile_options(${PROJECT_NAME} PRIVATE ${CFLAGS})

# Add Target Compile Include Path
#target_include_directories(${PROJECT_NAME} PRIVATE ${INCS})