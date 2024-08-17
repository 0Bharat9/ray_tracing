cmake_minimum_required(VERSION 3.10)
project(RayTracingInOneWeekend)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Create the executable and specify source files
add_executable(inOneWeekend src/main.cc)

# Include directories
target_include_directories(inOneWeekend PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

# Set the output directory for different build configurations (Debug, Release)
set_target_properties(
  inOneWeekend
  PROPERTIES RUNTIME_OUTPUT_DIRECTORY_DEBUG ${CMAKE_BINARY_DIR}/Debug
             RUNTIME_OUTPUT_DIRECTORY_RELEASE ${CMAKE_BINARY_DIR}/Release)
