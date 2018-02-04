# What version of CMake is needed?
cmake_minimum_required(VERSION 2.8.3)

# Name of this package
project(turtle_control_basic)

# Find the catkin build system, and any other packages on which we depend
find_package(catkin REQUIRED COMPONENTS roscpp geometry_msgs)

## Declare our catkin package
catkin_package()

# Specify locations of header files
include_directories(include ${catkin_INCLUDE_DIRS})

# For each executable provided by this package:
# add_executable: Declare the executable by specifying its source files.
# target_link_libraries: Specify libraries against which to link.
add_executable(turtle_control_basic_node src/turtle_control_basic_node.cpp)
target_link_libraries(turtle_control_basic_node ${catkin_LIBRARIES})
