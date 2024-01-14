# TIRT-Gazebo-Simple

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Ubuntu:Focal](https://img.shields.io/badge/Ubuntu-Focal-brightgreen)](https://releases.ubuntu.com/focal/)
[![ROS:Noetic](https://img.shields.io/badge/ROS-Noetic-blue)](https://wiki.ros.org/noetic/Installation/Ubuntu)

<kbd> <br> [English][en] <br> </kbd>
<kbd> <br> [简体中文][zh-CN] <br> </kbd>
<kbd> <br> 繁體中文 <br> </kbd>

[en]: README.md
[zh-CN]: README_zh-CN.md

“tirt_gazebo” ROS 軟體套件旨在為 TIRT 智慧服務競賽 - 送餐機器人提供簡易的模擬驗證工具。

## 軟體需求

- Gazebo
   ```
   sudo apt-get install gazebo11 && sudo apt-get install libgazebo11-dev
   ```
- Turtlebot3
   ```
   sudo apt-get install ros-noetic-turtlebot3*
   ```

## 安裝並建置

1. 導覽至您的 catkin 工作空間內的「src」目錄：
   ```
   cd ~/catkin_ws/src
   ```
2. 從 GitHub 複製 tirt_gazebo 套件至本地端：
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple.git tirt_gazebo
   ```
3. 建置 tirt_gazebo 套件：
   ```
   cd ~/catkin_ws && catkin_make
   ```
4. 套件環境設定：
   ```
   source ./devel/setup.sh
   ```

## 使用方法

1. 新增永久性工作空間環境變量：

   註：「{TURTLEBOT3_MODEL}」代表所使用的模型名稱：「burger」、「waffle」或「waffle_pi」。
   ```
   echo "export TURTLEBOT3_MODEL={TURTLEBOT3_MODEL}" >> ~/.bashrc
   ```
   ```
   source ~/.bashrc
   ```
2. 啟動模擬世界：
   ```
   roslaunch tirt_gazebo turtlebot3_tirt.launch
   ```
   
## 參考資料

- Ubuntu install of ROS Noetic (https://wiki.ros.org/noetic/Installation/Ubuntu)
- Install Gazebo using Ubuntu packages (https://classic.gazebosim.org/tutorials?tut=install_ubuntu)
- TurtleBot3 Simulation (https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/)
- TIRT (https://www.tirtpointsrace.org/)