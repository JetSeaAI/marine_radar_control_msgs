cmake_minimum_required(VERSION 3.5)
project(marine_radar_control_msgs)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)

set(msg_files
  "msg/RadarControlItem.msg"
  "msg/RadarControlSet.msg"
  "msg/RadarControlValue.msg"
)

rosidl_generate_interfaces(${PROJECT_NAME}
  ${msg_files}
  DEPENDENCIES std_msgs
)

ament_export_dependencies(rosidl_default_runtime)

ament_package()
