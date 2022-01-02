cmake_minimum_required(VERSION 3.22)


set(CMAKE_C_COMPILER "gcc")
set(CMAKE_CXX_COMPILER "g++")

# set the project name
project(BasicHttpClient)

# include directories
# include_directories(include)
include_directories("c:/asio-1.20.0/include/")

set(SOURCES src/main.cpp)

# add the executable
add_executable(BasicHttpClient ${SOURCES})
if(MINGW)
  target_link_libraries(BasicHttpClient ws2_32)
endif()