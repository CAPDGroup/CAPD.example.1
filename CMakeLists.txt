cmake_minimum_required(VERSION 3.13)
project(capd_example)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS YES)

file(GLOB SOURCES_LIST src/*.cpp)
add_executable(${PROJECT_NAME} ${SOURCES_LIST})

find_package(capd REQUIRED)
target_link_libraries(${PROJECT_NAME} PRIVATE -static capd::capd)
