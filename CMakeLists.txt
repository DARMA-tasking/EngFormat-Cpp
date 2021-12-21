project(EngFormat-Cpp CXX)
cmake_minimum_required(VERSION 3.0)

add_library(EngFormat-Cpp include/eng_format.hpp src/eng_format.cpp)

target_include_directories(EngFormat-Cpp PUBLIC
  $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include>
  $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>)

if(CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)
  include(CTest)
endif()

if(BUILD_TESTING)
  add_subdirectory(test)
endif()

