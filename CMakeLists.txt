CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
PROJECT(tflite_inference)
SET(CMAKE_BUILD_TYPE Debug)
SET(CMAKE_VERBOSE_MAKEFILE true)
SET(CMAKE_C_COMPILER "g++")
ADD_COMPILE_OPTIONS (  -g   -Wall -std=c++11 )
SET (CMAKE_EXE_LINKER_FLAGS "-Wl,--gc-sections")
INCLUDE_DIRECTORIES(./ ./flatbuffers/include)
LINK_DIRECTORIES(./lib/)
LINK_LIBRARIES(tensorflowlite)
ADD_EXECUTABLE(tflite_inference ./inference.cpp)