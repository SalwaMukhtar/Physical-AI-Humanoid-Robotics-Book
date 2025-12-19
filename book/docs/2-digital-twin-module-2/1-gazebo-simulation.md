---
sidebar_position: 1
---

# Gazebo Physics Simulation

Gazebo is a powerful 3D robotics simulator. It accurately simulates robots and their environments, providing a robust physics engine and a suite of sensors. Gazebo is widely used in the ROS community for developing and testing robot algorithms.

## Key Features of Gazebo

-   **Physics Engine**: Gazebo includes high-quality physics engines (e.g., ODE, Bullet, Simbody, DART) that allow for realistic simulation of rigid body dynamics, gravity, and contacts.
-   **3D Visualization**: It provides an accurate visual representation of the robot and its environment, which is crucial for debugging and understanding robot behavior.
-   **Sensor Simulation**: Gazebo can simulate a variety of sensors, including cameras, LiDAR, IMUs, force/torque sensors, and more. This allows developers to test their perception algorithms without needing physical hardware.
-   **Plugins**: Gazebo's functionality can be extended through plugins, allowing users to create custom sensors, actuators, and world dynamics.

## Launching a Simple Gazebo Simulation

To launch a simple Gazebo simulation with ROS 2, you typically use `ros2 launch` with a launch file. A launch file in ROS 2 uses Python or XML to define and run multiple nodes and processes.

Here's an example of how you might launch a basic Gazebo world:

First, make sure you have Gazebo installed and sourced your ROS 2 environment.

```bash
# Example: Install Gazebo for ROS 2 Humble
sudo apt update
sudo apt install ros-humble-gazebo-ros-pkgs ros-humble-desktop
```

A minimal launch file (`my_robot_world.launch.py`) might look like this:

```python
import os
from ament_index_python.packages import get_package_share_directory
from launch import LaunchDescription
from launch.actions import IncludeLaunchDescription
from launch.launch_description_sources import PythonLaunchDescriptionSource

def generate_launch_description():
    pkg_gazebo_ros = get_package_share_directory('gazebo_ros')
    
    # We want to use the 'empty.world' from Gazebo's default worlds
    gazebo_world_path = os.path.join(
        get_package_share_directory('gazebo_msgs'),
        'share',
        'gazebo_msgs',
        'worlds',
        'empty.world'
    )

    return LaunchDescription([
        IncludeLaunchDescription(
            PythonLaunchDescriptionSource(
                os.path.join(pkg_gazebo_ros, 'launch', 'gazebo.launch.py')
            ),
            launch_arguments={'world': gazebo_world_path}.items(),
        ),
    ])
```

You would then launch this using:

```bash
ros2 launch your_package_name my_robot_world.launch.py
```

This command would start Gazebo with an empty world, ready for you to spawn your robot models.
