# ROS 1 + Ignition Gazebo demos

This package contains demos showing how to use Ignition Gazebo with ROS 1.

details: https://products.rt-net.jp/micromouse/archives/8833

## Usage

Send commands to a differential drive vehicle and listen to its odometry.

    roslaunch ros_ign_gazebo_raspimouse raspimouse.launch

Then send a command

    rostopic pub /model/raspimouse/cmd_vel geometry_msgs/Twist "{linear: {x: 0.1}, angular: {z: 0.1}}"

![](https://products.rt-net.jp/micromouse/wp-content/uploads/sites/3/2019/10/Rec-2019-10-06_21.19.28.gif)

## License

(C) 2019 Tiryoh

This repository is released under the Apache License 2.0, see [LICENSE](./LICENSE).
Unless attributed otherwise, everything in this repository is under the Apache License 2.0.

### Acknowledgements

This repository is delivered from `ros_ign_gazebo_demo` in [osrf/ros_ign](https://github.com/osrf/ros_ign).  
by Open Robotics, licensed under the Apache License 2.0.
