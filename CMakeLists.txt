cmake_minimum_required(VERSION 3.5)

project(ros_ign_gazebo_raspimouse)

find_package(catkin REQUIRED)
find_package(ignition-gazebo2 2.1 QUIET REQUIRED)

catkin_package()

catkin_add_env_hooks(ign SHELLS bash
  DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)
catkin_add_env_hooks(ign SHELLS zsh
  DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)

install(
  PROGRAMS
    scripts/ign_gazebo
    scripts/configure_models
  DESTINATION
    ${CATKIN_PACKAGE_BIN_DESTINATION})

install(
  DIRECTORY
    launch/
  DESTINATION
    ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)

install(
  DIRECTORY
    rviz/
  DESTINATION
    ${CATKIN_PACKAGE_SHARE_DESTINATION}/rviz
)

install(
  DIRECTORY
    worlds/
  DESTINATION
    ${CATKIN_PACKAGE_SHARE_DESTINATION}/worlds
)
