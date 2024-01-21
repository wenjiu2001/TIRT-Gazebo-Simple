# TIRT-Gazebo-Simple

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Ubuntu:Focal](https://img.shields.io/badge/Ubuntu-Focal-brightgreen)](https://releases.ubuntu.com/focal/)
[![ROS:Noetic](https://img.shields.io/badge/ROS-Noetic-blue)](https://wiki.ros.org/noetic/Installation/Ubuntu)

<kbd> <br> [English][en] <br> </kbd>
<kbd> <br> 简体中文 <br> </kbd>
<kbd> <br> [繁體中文][zh-TW] <br> </kbd>

[en]: README.md
[zh-TW]: README_zh-TW.md

“tirt_gazebo” ROS 软件包旨在为 TIRT 智慧服务竞赛 - 送餐机器人组提供简便的仿真验证工具。

## 软件依赖

- Gazebo
   ```
   sudo apt-get install gazebo11 && sudo apt-get install libgazebo11-dev
   ```
- Turtlebot3
   ```
   sudo apt-get install ros-noetic-turtlebot3*
   ```

## 安装并构建

1. 导航至您的 catkin 工作空间内的「src」目录：
   ```
   cd ~/catkin_ws/src
   ```
2. 从 GitHub 克隆 tirt_gazebo 包至本地端：
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple.git tirt_gazebo
   ```
3. 构建 tirt_gazebo 包：
   ```
   cd ~/catkin_ws && catkin_make
   ```
4. 包环境设置：
   ```
   source ./devel/setup.sh
   ```

## 使用方法

通过修改以下参数可以进行调整：

| 参数名称 | 数据类型 | 详细信息                                       |
| -------- | -------- | ---------------------------------------------- |
| model    | 字符串   | 设置Turtlebot3机器人模型。 <br/>默认值：`null` |
| x_pos    | 浮点数   | 设置机器人的初始X轴位置。 <br/>默认值：`0.0`   |
| y_pos    | 浮点数   | 设置机器人的初始Y轴位置。 <br/>默认值：`2.7`   |
| z_pos    | 浮点数   | 设置机器人的初始Z轴位置。 <br/>默认值：`0.0`   |

1. 添加永久性工作空间环境变量：

   - Turtlebot3模型

      - Burger
        ```
        echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
        ```
      - Waffle
        ```
        echo "export TURTLEBOT3_MODEL=waffle" >> ~/.bashrc
        ```
      - Waffle Pi
        ```
        echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc
        ```
   - 重新加载 .bashrc 文件
     ```
     source ~/.bashrc
     ```
2. 启动仿真世界：
   ```
   roslaunch tirt_gazebo turtlebot3_tirt.launch
   ```
   
## 参考资料

- [在Ubuntu上安装ROS Noetic](https://wiki.ros.org/noetic/Installation/Ubuntu)
- [使用Ubuntu软件包安装Gazebo](https://classic.gazebosim.org/tutorials?tut=install_ubuntu)
- [TurtleBot3 仿真](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/)
- [TIRT](https://www.tirtpointsrace.org/)
