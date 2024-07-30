cmake_minimum_required(VERSION 3.0.2)
project(astar_ros_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)
find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
  nav_msgs
  )

add_service_files(
  FILES
  GetPlan.srv
)

generate_messages(
  DEPENDENCIES
  geometry_msgs  nav_msgs
)
catkin_package(
  CATKIN_DEPENDS geometry_msgs message_runtime nav_msgs
)
