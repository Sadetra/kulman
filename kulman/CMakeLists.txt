cmake_minimum_required(VERSION 2.8.3)
project(kulman)

add_definitions("-std=c++11")

find_package(catkin REQUIRED
  COMPONENTS
  kulman_basics
  kulman_controller_frame
  kulman_controller
  kulman_joystick
  kulman_model
  kulman_msgs
  kulman_rviz
  kulman_state_estimator
  param_io
)

catkin_package(
  CATKIN_DEPENDS
    kulman_basics
    param_io
)
