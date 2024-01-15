# TIRT-Gazebo-Simple

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Ubuntu:Focal](https://img.shields.io/badge/Ubuntu-Focal-brightgreen)](https://releases.ubuntu.com/focal/)
[![ROS:Noetic](https://img.shields.io/badge/ROS-Noetic-blue)](https://wiki.ros.org/noetic/Installation/Ubuntu)

<kbd> <br> English <br> </kbd>
<kbd> <br> [简体中文][zh-CN] <br> </kbd>
<kbd> <br> [繁體中文][zh-TW] <br> </kbd>

[zh-CN]: README_zh-CN.md
[zh-TW]: README_zh-TW.md

The "tirt_gazebo" ROS package is crafted with the objective of facilitating uncomplicated simulation validation for the TIRT Intelligent Service Competition - Food Runner Robots.

## Requirements

- Gazebo
   ```
   sudo apt-get install gazebo11 && sudo apt-get install libgazebo11-dev
   ```
- Turtlebot3
   ```
   sudo apt-get install ros-noetic-turtlebot3*
   ```

## Install and Build

1. Navigating to the "src" directory within your catkin workspace :
   ```
   cd ~/catkin_ws/src
   ```
2. Clone tirt_gazebo package for github :
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple.git tirt_gazebo
   ```
3. Build tirt_gazebo package :
   ```
   cd ~/catkin_ws && catkin_make
   ```
4. Package environment setup :
   ```
   source ./devel/setup.sh
   ```

## How to Use

Adjustments can be made by modifying the following parameters:

| Parameter name | Data Type | Detail                                                            |
| -------------- | --------- | ----------------------------------------------------------------- |
| model          | string    | Set the Turtlebot3 robot model. <br/>default: `null`              |
| x_pos          | float     | Set the initial X-axis position of the robot. <br/>default: `0.0` |
| y_pos          | float     | Set the initial Y-axis position of the robot. <br/>default: `2.7` |
| z_pos          | float     | Set the initial Z-axis position of the robot. <br/>default: `0.0` |

1. Add permanent workspace environment variables :

   Note: "{TURTLEBOT3_MODEL}" represents the name of the utilized models: "burger", "waffle", or "waffle_pi".
   ```
   echo "export TURTLEBOT3_MODEL={TURTLEBOT3_MODEL}" >> ~/.bashrc
   ```
   ```
   source ~/.bashrc
   ```
2. Launch Simulation World :
   ```
   roslaunch tirt_gazebo turtlebot3_tirt.launch
   ```
   
## References

- Ubuntu install of ROS Noetic (https://wiki.ros.org/noetic/Installation/Ubuntu)
- Install Gazebo using Ubuntu packages (https://classic.gazebosim.org/tutorials?tut=install_ubuntu)
- TurtleBot3 Simulation (https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/)
- TIRT (https://www.tirtpointsrace.org/)
