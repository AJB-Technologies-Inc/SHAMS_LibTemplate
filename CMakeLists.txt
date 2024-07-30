cmake_minimum_required(VERSION 3.16)

project(SHAMS_Lib)

# Force the user to change the project name
if(PROJECT_NAME STREQUAL "SHAMS_Lib")
    message(FATAL_ERROR "The project name is still set to the default 'SHAMS_Lib'. Please update the project name in the root CMakeLists.txt file.")
endif()

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add other cmake files
include(cmake/install_libs.cmake)

# Add the Events library
add_subdirectory(source/)

# Enable testing and add the test directory
if(CMAKE_SOURCE_DIR STREQUAL PROJECT_SOURCE_DIR)
	enable_testing()
	add_subdirectory(test)
endif()
