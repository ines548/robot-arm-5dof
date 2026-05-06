# ROS2 Robot Arm Project

##  Overview

This project implements the **SO-100 robotic arm** using ROS2, including:

* URDF robot model
* RViz visualization
* Gazebo simulation (experimental)
* MoveIt2 integration
* Controller architecture (ros2_control)

The goal is to build a **Pick & Place robotic system with vision (YOLO)**.

## Pick and place motion wanted
<img width="320" height="170" alt="rviz_pnp" src="https://github.com/user-attachments/assets/b40d3c37-4623-4c25-9df9-9ae7adb211ec" />




## Features

* 5/6 DOF robotic arm simulation
* Real-time joint visualization in RViz
* ROS2 control architecture
* Gazebo simulation support (WIP)
* MoveIt2 motion planning

---

##  Workspace Structure

```
ros2_ws/
├── src/
│   ├── so_arm_100/
│   ├── so_arm_100_bringup/
│   ├── so_arm_100_description/
│   ├── so_arm_100_moveit_config/
│   └── so_arm_100_hardware/
```

---

##  Installation

```bash
cd ~/ros2_ws
rosdep install --from-paths src --ignore-src -r -y
colcon build
source install/setup.bash
```

---

##  Run RViz Visualization

```bash
ros2 launch so_arm_100_bringup rviz.launch.py
```

---

##  Run MoveIt (motion planning)

```bash
ros2 launch so_arm_100_moveit_config demo.launch.py
```

---

## Visualisation i got 
<img width="1213" height="801" alt="Screenshot from 2026-05-06 20-59-17" src="https://github.com/user-attachments/assets/9e5b944a-4e41-44db-98c5-a5116f830cac" />




##  Current Issues

* Gazebo simulation may crash (physics plugin issue)
* ros2_control needs tuning for Gazebo Sim



##  Future Work

* YOLO object detection integration
* Camera-based pick & place
* Raspberry Pi deployment
* Real hardware control

