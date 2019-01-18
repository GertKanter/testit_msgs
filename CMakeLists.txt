cmake_minimum_required(VERSION 2.8.3)
project(testit_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
)

add_message_files(
  DIRECTORY msg
    FILES
    FileCoverage.msg)

add_service_files(
  DIRECTORY srv
  FILES
  Coverage.srv
)

generate_messages(
  # DEPENDENCIES
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)
