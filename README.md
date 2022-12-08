# gps-waypoint-based-autonomous-navigation-in-ros-tutorial

# pre - Settup

- Robot_Localization
  - cd catkin_ws/src
  - git clone https://github.com/cra-ros-pkg/robot_localization.git
  ---
  - 수정경로?
  - cd catkin_ws/src/include/robot_localization

# Settup : gps-waypoint-based-autonomous-navigation-in-ros
- cd catkin_ws/src
- git clone https://github.com/ArghyaChatterjee/gps-waypoint-based-autonomous-navigation-in-ros.git gps_waypoint_nav

## 수정사항
- CMakeList.txt
  - cd catkin_ws/src/gps-waypoint-nva
  - gedit CMakeLists.txt
    
    find_package(catkin REQUIRED COMPONENTS
      roscpp
      rospy
      std_msgs
      tf
      roslib
      roslaunch
      robot_localization //추가, 근데 이미 추가되어있었음
      )
      
- Package.xml 
  - cd catkin_ws/src/gps-waypoint-based-autonomous-navigation-in-ros
  - gedit package.xml
  
    <buildtool_depend>catkin</buildtool_depend>
    <build_depend>roscpp</build_depend>
    <build_depend>rospy</build_depend>
    <build_depend>std_msgs</build_depend>
    <build_depend>roslaunch</build_depend>
    <build_depend>robot_localization</build_depend> // 이것도 이미 추가되어있었음
    
- .CPP
  - 변경할 항목
    - gps_waypoint.cpp
    - gps_waypoint_continuous1.cpp
    - gps_waypoint_continuous2.cpp
    - gps_waypoint_mapping.cpp
    - plot_gps_waypoints.cpp

  -  #include <robot_localization/navsat_conversions.h>
  
    - #include "/ _your_path_ /catkin_ws/src/robot_localization/include/robot_localization/navsat_conversions.h"
