cmake_minimum_required(VERSION 3.5)
project(HelloApp
       VERSION 0.0.1
       DESCRIPTION "TheTestName"
       LANGUAGES CXX)
#add_executable(HelloAppBinary main.cpp src/dog.cpp src/operations.cpp)
file(GLOB_RECURSE SOURCE_FILES src/*.cpp)

add_executable(HelloAppBinary main.cpp ${SOURCE_FILES})


target_compile_features(HelloAppBinary PRIVATE cxx_std_23)
target_include_directories(HelloAppBinary PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)