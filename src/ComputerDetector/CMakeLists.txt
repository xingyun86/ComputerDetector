cmake_minimum_required(VERSION 3.4)
project(ComputerDetector CXX)

add_subdirectory(src/x86)
target_include_directories(ComputerDetector PUBLIC src)
if(CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)
    add_executable(ComputerDetector_main src/Main.cpp)
    target_link_libraries(ComputerDetector_main PUBLIC ComputerDetector)
endif()
