cmake_minimum_required(VERSION 3.5)

project(demoOpen62541)

set (EXECUTABLE_OUTPUT_PATH  ${PROJECT_SOURCE_DIR}/bin)

add_definitions(-std=c99)

include_directories(${PROJECT_SOURCE_DIR}/open62541)

add_executable(server ${PROJECT_SOURCE_DIR}/src/server.c ${PROJECT_SOURCE_DIR}/open62541/open62541.c)

add_executable(client ${PROJECT_SOURCE_DIR}/src/client.c ${PROJECT_SOURCE_DIR}/open62541/open62541.c)