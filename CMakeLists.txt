cmake_minimum_required( VERSION 3.12 )
project(multi_tracker_msgs)

find_package(catkin REQUIRED COMPONENTS 
                message_generation 
                std_msgs
                sensor_msgs)

add_message_files(DIRECTORY msg
                FILES
                AngledBox.msg
                AngledBoxArray.msg
                MaskArray.msg
)

generate_messages(DEPENDENCIES std_msgs sensor_msgs)

catkin_package(CATKIN_DEPENDS message_runtime std_msgs sensor_msgs)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
