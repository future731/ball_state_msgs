cmake_minimum_required(VERSION 2.8.3)
project(ball_state_msgs)

find_package(catkin REQUIRED COMPONENTS
    roscpp roseus rospy message_generation std_msgs geometry_msgs
)

add_message_files(
    FILES
    PosAndVelWithCovarianceStamped.msg
    Log.msg
)

generate_messages(DEPENDENCIES
    std_msgs geometry_msgs
)

catkin_package(CATKIN_DEPENDS
    message_runtime
)
