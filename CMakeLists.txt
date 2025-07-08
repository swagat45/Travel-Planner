cmake_minimum_required(VERSION 3.15)
project(TravelPlanner)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED YES)

# Enable warnings and AddressSanitizer in Debug builds
if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Debug)
endif()

if (CMAKE_BUILD_TYPE STREQUAL "Debug")
  add_compile_options(-Wall -Wextra -fsanitize=address)
  add_link_options(-fsanitize=address)
endif()

add_executable(planner
    Main.cpp
)


target_include_directories(planner PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
