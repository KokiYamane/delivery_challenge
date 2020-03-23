# gazebo
source ./install/local_setup.bash
roslaunch delivery_challenge_simulation create_stage.launch gui:=trueh


# robot application
cd robot_ws
source ./install/local_setup.bash
roslaunch src/delivery_robot_sample/launch/navigation_robot.launch


# rviz
roslaunch robot_ws/src/delivery_robot_sample/launch/rviz_for_navigation.launch


# build
colcon build
