cmake_minimum_required (VERSION 3.16..3.24)

set (CMAKE_CXX_STANDARD 17)

project (__PROJECT_NAME__ VERSION 0.0.1
  DESCRIPTION "My awesome project"
                LANGUAGES CXX)

# Update the submodules automatically
include (cmake/UpdateSubmodules.cmake)

# Enable testing for this project
include (CTest)

# Add subdirectories with code
add_subdirectory (external)
add_subdirectory (__PROJECT_NAME__)
add_subdirectory (test)

