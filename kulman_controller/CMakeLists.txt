cmake_minimum_required(VERSION 2.8.3)
project(kulman_controller)

add_definitions("-std=c++11")

find_package(catkin REQUIRED
  COMPONENTS
)

catkin_package(
  INCLUDE_DIRS
  	include
  LIBRARIES
  CATKIN_DEPENDS
)


# if  ${catkin_INCLUDE_DIRS} is not added, c code in can't find headers from other
# packages
# if  inclde is not added, c code in can't find headers from this package can't be
# found
include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)


#add_library(
#  ${PROJECT_NAME}
#)

#add_dependencies(${PROJECT_NAME}
#  ${catkin_EXPORTED_TARGETS}
#)
#target_link_libraries(${PROJECT_NAME}
#  ${catkin_LIBRARIES}
#  ${Boost_LIBRARIES}
#)
