cmake_minimum_required(VERSION 3.0.2)
project(ur5_gpd)

find_package(catkin REQUIRED COMPONENTS
roscpp
  rospy
  std_msgs
  gazebo_ros
  message_generation
  sensor_msgs)
 
  
generate_messages(
   DEPENDENCIES
   std_msgs
)

catkin_package(DEPENDS 
    CATKIN_DEPENDS roscpp rospy std_msgs message_runtime
    CATKIN_DEPENDS roscpp sensor_msgs
    INCLUDE_DIRS
    LIBRARIES )

include_directories(include ${catkin_INCLUDE_DIRS})
