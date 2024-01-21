# TIRT-Gazebo-Simple

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Ubuntu:Focal](https://img.shields.io/badge/Ubuntu-Focal-brightgreen)](https://releases.ubuntu.com/focal/)
[![ROS:Noetic](https://img.shields.io/badge/ROS-Noetic-blue)](https://wiki.ros.org/noetic/Installation/Ubuntu)

<kbd> <br> [English][en] <br> </kbd>
<kbd> <br> [简体中文][zh-CN] <br> </kbd>
<kbd> <br> 繁體中文 <br> </kbd>

[en]: README.md
[zh-CN]: README_zh-CN.md

“tirt_gazebo” ROS 軟體套件旨在為 TIRT 智慧服務競賽 - 送餐機器人組提供簡易的模擬驗證工具。

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

透過修改以下參數可以進行調整：

| 參數名稱 | 資料類型 | 詳細資訊                                       |
| -------- | -------- | ---------------------------------------------- |
| model    | 字串     | 設定Turtlebot3機器人模型。 <br/>預設值：`null` |
| x_pos    | 浮點數   | 設定機器人的初始X軸位置。 <br/>預設值：`0.0`   |
| y_pos    | 浮點數   | 設定機器人的初始Y軸位置。 <br/>預設值：`2.7`   |
| z_pos    | 浮點數   | 設定機器人的初始Z軸位置。 <br/>預設值：`0.0`   |

1. 新增永久性工作空間環境變量：

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
   - 重新載入 .bashrc 文件
     ```
     source ~/.bashrc
     ```
2. 啟動模擬世界：
   ```
   roslaunch tirt_gazebo turtlebot3_tirt.launch
   ```
   
## 參考資料

- [在Ubuntu上安裝ROS Noetic](https://wiki.ros.org/noetic/Installation/Ubuntu)
- [使用Ubuntu套件安裝Gazebo](https://classic.gazebosim.org/tutorials?tut=install_ubuntu)
- [TurtleBot3 模擬](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/)
- [TIRT](https://www.tirtpointsrace.org/)
