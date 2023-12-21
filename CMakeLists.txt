# Project Name
PROJECT(DigitalCamera)
cmake_minimum_required(VERSION 2.8)

# Set the output folder where your program will be created
set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})

# Find OpenCV, you may need to set OpenCV_DIR variable
# to the absolute path to the directory containing OpenCVConfig.cmake file
# via the command line or GUI
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})
# Add optional header files from inc/ directory
include_directories(inc)
# Executable
add_executable(DigitalCamera src/main.cpp)
# Link your application with OpenCV libraries
link_directories(${OpenCV_LIBRARY_DIRS})
target_link_libraries(DigitalCamera ${OpenCV_LIBS})


