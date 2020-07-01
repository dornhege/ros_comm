cmake_minimum_required(VERSION 3.0.2)
project(rosparam)
if(NOT CMAKE_CONFIGURATION_TYPES AND NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

find_package(catkin REQUIRED)
catkin_package()

catkin_python_setup()
