# TIRT-Gazebo-Simple

[![Lifecycle:Stable](https://img.shields.io/badge/Lifecycle-Stable-97ca00)](<Redirect-URL>)
[![License](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

The "tirt_gazebo" ROS package is crafted with the objective of facilitating uncomplicated simulation validation for the TIRT Intelligent Service Competition - Food Runner Robots.

## Environment

- Ubuntu 20.04
- ROS Noetic

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
1. Choosing a robotic model :

   Note: "{TURTLEBOT3_MODEL}" represents the name of the utilized models: "burger", "waffle", or "waffle_pi".
   ```
   export TURTLEBOT3_MODEL={TURTLEBOT3_MODEL}
   ```
   Add permanent workspace environment variables.
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
