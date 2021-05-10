# robotics_project_001
ROS2 Multi-robot simulation

Note: Please follow the following sequence

**For Mapping :**

1) Launch simulation
```ros2 launch robot_simulation gazebo_world.launch.py```

2) Rviz launch 
```ros2 launch robot_slam rviz.launch.py``` 
(No visulization will be updated and ignore the rviz errors, since map to robot frame is not available)

3) Teleop :
```ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r cmd_vel:=/robot/cmd_vel```

4)Mapping launch 
```ros2 launch robot_slam mapping.launch.py```
(use the 2d_estimated_pose button in rviz to give the robot the initial pose estimate)


**For Navigation :** 

1) Launch simulation
```ros2 launch robot_simulation gazebo_world.launch.py```

2) Rviz launch 
```ros2 launch robot_slam rviz.launch.py``` 
(No visulization will be updated and ignore the rviz errors, since map to robot frame is not available)

3) Localization launch 
```ros2 launch robot_slam localization.launch.py```
(use the 2d_estimated_pose button in rviz to give the robot the initial pose estimate)

4) navigation launch 
```ros2 launch robot_slam navigation.launch.py```

5) Teleop :
```ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r cmd_vel:=/robot/cmd_vel```


resources:
- [multi-robot-experiments](https://discourse.ros.org/t/giving-a-turtlebot3-a-namespace-for-multi-robot-experiments/10756)