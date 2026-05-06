# ROS2 Robot Arm Project

##  Overview

This project implements the **SO-100 robotic arm** using ROS2, including:

* URDF robot model
* RViz visualization
* Gazebo simulation (experimental)
* MoveIt2 integration
* Controller architecture (ros2_control)

The goal is to build a **Pick & Place robotic system with vision (YOLO)**.



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




##  Current Issues

* Gazebo simulation may crash (physics plugin issue)
* ros2_control needs tuning for Gazebo Sim



##  Future Work

* YOLO object detection integration
* Camera-based pick & place
* Raspberry Pi deployment
* Real hardware control

