cmake_minimum_required(VERSION 3.5)

project(qt_test LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
file(GLOB ALLHEADERS ${CMAKE_CURRENT_SOURCE_DIR}/*.h)#将文件夹下所有头文件加入
find_package(Qt5Core)

add_executable(qt_test
  main.cpp another.cpp
  ${ALLHEADERS}
)
target_link_libraries(qt_test Qt5::Core)
