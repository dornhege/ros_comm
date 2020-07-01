cmake_minimum_required(VERSION 3.0.2)
project(rosnode)
if(NOT CMAKE_CONFIGURATION_TYPES AND NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

find_package(catkin REQUIRED)
catkin_package()

catkin_python_setup()

if(CATKIN_ENABLE_TESTING)
  find_package(rostest)
  add_rostest(test/rosnode.test)
endif()
