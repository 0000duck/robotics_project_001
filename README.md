# robotics_project_001
ROS2 Multi-robot simulation

Launch simulation
```ros2 launch robot_simulation gazebo_world.launch.py```

Teleop :
```ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r cmd_vel:=/robot/cmd_vel```


resources:
- [multi-robot-experiments](https://discourse.ros.org/t/giving-a-turtlebot3-a-namespace-for-multi-robot-experiments/10756)