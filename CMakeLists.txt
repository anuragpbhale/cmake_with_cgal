# CMake starter for C++17

cmake_minimum_required( VERSION 3.26 )
project( project_name CXX )

# Set Environment variables used by CMAke.
set( CMAKE_CXX_STANDARD 17 )
set( CMAKE_CXX_STANDARD_REQUIRED ON )
set( CMAKE_CXX_FLAGS_DEBUG "-Wall -Wextra -frounding-math" )  
set( CMAKE_BUILD_TYPE Debug )
set( CGAL_DO_NOT_WARN_ABOUT_CMAKE_BUILD_TYPE TRUE )

# Set the source file. 
# Multiple source files can be included with a space.

find_package(CGAL)

set( SRCS src/Source.cpp )

# include directories for the include folder and libraries folder.
include_directories( $(include/) )
include_directories( $(lib/) )

# add source files to the project.
add_executable( project_name ${SRCS} )

link_libraries(project_name PRIVATE CGAL::CGAL)
