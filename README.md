# bot_spawn ROS2 Package

This repository contains the `bot_spawn` ROS2 package, designed for spawning a robot model in the Gazebo simulator. The package includes URDF descriptions for various components such as camera, depth camera, lidar, and robot core. Additionally, it provides control configurations and launch files for simulation setup.
## Prerequisites

Before launching the `bot_spawn` package, make sure you have the following ROS 2 packages installed:

- [ros-humble-gazebo-ros-pkgs](https://index.ros.org/p/ros-humble-gazebo-ros-pkgs/): ROS integration with Gazebo simulator.
- [ros-humble-ros2-control](https://index.ros.org/p/ros-humble-ros2-control/): ROS 2 control system.
- [ros-humble-ros2-controllers](https://index.ros.org/p/ros-humble-ros2-controllers/): ROS 2 controller packages.
- [ros-humble-gazebo-ros2-control](https://index.ros.org/p/ros-humble-gazebo-ros2-control/): ROS 2 integration with Gazebo for control.
- [ros-humble-slam-toolbox](https://index.ros.org/p/ros-humble-slam-toolbox/): Toolbox for SLAM (Simultaneous Localization and Mapping).
- [ros-humble-navigation2](https://index.ros.org/p/ros-humble-navigation2/): Navigation system for ROS 2.

You can install these packages using `rosdep` or through the ROS 2 package manager:

```bash
rosdep install --from-paths src --ignore-src -r -y
```
## Installation

To install and utilize the `bot_spawn` package, follow these steps:

1. **Create Workspace:** Create a workspace folder named `ros2_ws` if you haven't already.

2. **Clone Repository:** Clone this repository into the `src` folder of your ROS2 workspace (`ros2_ws/src/`).

3. **Build:** Navigate to the root of your workspace (`ros2_ws/`) and build the packages using the following command:
    ```bash
    colcon build
    ```

4. **Source Setup Script:** After successful build, source the setup script to add the package to your ROS2 environment:
    ```bash
    source install/setup.bash
    ```

## Usage

To launch the Gazebo simulation with the robot model, execute the following command:

```bash
ros2 launch bot_spawn gazebo.launch.py
