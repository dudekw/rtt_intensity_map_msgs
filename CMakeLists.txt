
cmake_minimum_required(VERSION 2.8.3)
project(rtt_intensity_map_msgs)

find_package(catkin REQUIRED COMPONENTS rtt_roscomm intensity_map_msgs)

ros_generate_rtt_typekit(intensity_map_msgs)
ros_generate_rtt_service_proxies(intensity_map_msgs)

orocos_generate_package(
  DEPENDS intensity_map_msgs
  DEPENDS_TARGETS rtt_roscomm rtt_std_msgs intensity_map_msgs
)
