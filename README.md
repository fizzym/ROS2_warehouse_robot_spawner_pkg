# ROS2_warehouse_robot_spawner_pkg

### Description
Builds a Gazebo world with a differential drive robot with laser scanner.

### Requirements
Requirements: Ubuntu 20.04; ROS2 Foxy;

### Instructions
To run clone in ros2_ws/src:
```
cd ~/ros2_ws/src
git clone https://github.com/fizzym/ROS2_warehouse_robot_spawner_pkg
```
Build the package using colcon and resource the environment:
```
cd ~/ros2_ws/
colcon build --packages-select warehouse_robot_spawner_pkg
source install/setup.bash
```
Launch the package:
```
ros2 launch warehouse_robot_spawner_pkg gazebo_world.launch.py 
```
To drive the robot from the keyboard run:
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args --remap /cmd_vel:=/demo/cmd_vel
```

### Reference
Implements Automatic Addison ["How to Simulate a Robot Using Gazebo and ROS 2"](https://automaticaddison.com/how-to-simulate-a-robot-using-gazebo-and-ros-2/).
