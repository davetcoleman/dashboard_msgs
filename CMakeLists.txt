cmake_minimum_required(VERSION 2.8.3)
project(dashboard_msgs)

set(MSG_DEPS
  std_msgs
)

find_package(catkin REQUIRED COMPONENTS
  genmsg ${MSG_DEPS}
)

add_message_files(DIRECTORY msg FILES 
  DashboardControl.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(DEPENDENCIES ${MSG_DEPS})

catkin_package(DEPENDS ${MSG_DEPS})

