# bot_spawn ROS2 Package

This repository contains the `bot_spawn` ROS2 package, designed for spawning a robot model in the Gazebo simulator. The package includes URDF descriptions for various components such as camera, depth camera, lidar, and robot core. Additionally, it provides control configurations and launch files for simulation setup.
## Prerequisites
Before launching the `bot_spawn` package, make sure you have the following ROS 2 packages installed:

### Dependencies
```bash
sudo apt update
```
```bash
sudo apt install ros-$ROS_DISTRO-gazebo-ros-pkgs ros-$ROS_DISTRO-ros2-control ros-$ROS_DISTRO-ros2-controllers ros-$ROS_DISTRO-gazebo-ros2-control ros-$ROS_DISTRO-slam-toolbox ros-$ROS_DISTRO-navigation2 ros-$ROS_DISTRO-xacro python3-colcon-common-extensions
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
5. **Download Models For Gazebo:(61mb)** extract this [models.zip](https://drive.google.com/file/d/1-vp-h2SC5LAaBPh5dM73qWktby505QeP/view?usp=sharing) to `/home/.gazebo/`. Name should be **models**.

## Usage

To launch the Gazebo simulation with the robot model, execute the following command:

```bash
ros2 launch bot_spawn gazebo.launch.py
```
To launch teleop:
```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_cont/cmd_vel_unstamped
```
