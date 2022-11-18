cmake_minimum_required(VERSION 3.24.1)

project(
  Project
  VERSION 1.0
  LANGUAGES CXX)

set(CMAKE_CXX_STANDARD
  17
  CACHE STRING "C++ STANDARD 11")
set(CMAKE_STANDARD_REQUIRED ON)
set(CMAKE_PLATFORM_INDEPENDENT_CODE ON)

add_subdirectory(src)
add_subdirectory(apps)
add_subdirectory(tests)

target_include_directories(${PROJECT_NAME} PUBLIC include)
target_link_directories(${PROJECT_NAME} PRIVATE src)

target_link_libraries(${PROJECT_NAME} lib anotherlib)
