# bot_spawn ROS2 Package

This repository contains the `bot_spawn` ROS2 package, designed for spawning a robot model in the Gazebo simulator. The package includes URDF descriptions for various components such as camera, depth camera, lidar, and robot core. Additionally, it provides control configurations and launch files for simulation setup.

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
