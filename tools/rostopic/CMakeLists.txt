cmake_minimum_required(VERSION 3.0.2)
project(rostopic)
if(NOT CMAKE_CONFIGURATION_TYPES AND NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

find_package(catkin REQUIRED)
catkin_package()

catkin_python_setup()

catkin_install_python(PROGRAMS scripts/rostopic
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

if(CATKIN_ENABLE_TESTING)
  find_package(rostest)
  add_rostest(test/rostopic.test)
  #add_rostest(test/rostopic2.test)
  catkin_add_nosetests(test/test_rostopic_command_line_offline.py)
endif()
