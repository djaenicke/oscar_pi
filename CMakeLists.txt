cmake_minimum_required(VERSION 3.0.2)
project(oscar_pi)

find_package(catkin REQUIRED COMPONENTS
  message_generation
)

add_message_files(
  FILES
  state.msg
  cmd.msg
)

generate_messages(
  DEPENDENCIES
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
