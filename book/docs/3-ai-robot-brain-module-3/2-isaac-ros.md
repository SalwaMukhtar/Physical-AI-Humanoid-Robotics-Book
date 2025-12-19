---
sidebar_position: 2
---

# Isaac ROS

NVIDIA Isaac ROS is a collection of GPU-accelerated packages designed to bring high-performance perception and AI capabilities to ROS 2. It leverages NVIDIA's extensive expertise in GPU computing to optimize common robotics tasks, making it ideal for advanced applications in humanoid robotics.

## Key Features of Isaac ROS

-   **GPU Acceleration**: Isaac ROS packages are highly optimized to run on NVIDIA GPUs, significantly accelerating computationally intensive tasks like image processing, deep learning inference, and VSLAM.
-   **VSLAM (Visual Simultaneous Localization and Mapping)**: Provides robust and accurate localization and mapping using visual input from cameras. Essential for robots operating in unknown or dynamic environments.
-   **Navigation**: Integrates with ROS 2 Nav2 stack, offering GPU-accelerated components for global and local planning, obstacle avoidance, and path following.
-   **Perception**: Includes modules for various perception tasks such as object detection, pose estimation, and segmentation, all optimized for NVIDIA hardware.
-   **Developer Tools**: Offers tools for debugging, visualization, and integrating with other NVIDIA platforms like Isaac Sim.

## Running Basic Isaac ROS VSLAM

To run a basic Isaac ROS VSLAM application, you typically use a pre-built graph or a sample application provided by NVIDIA. This often involves:

1.  **Setting up the Environment**: Ensure you have a compatible ROS 2 distribution (e.g., Humble) and the necessary NVIDIA drivers, CUDA, and cuDNN installed. Isaac ROS typically runs within a Docker container for easier dependency management.
2.  **Launching the VSLAM Node**: Start the VSLAM node, often integrated with a camera driver (real or simulated). This node will take camera images as input.
3.  **Visualization**: Use RViz or another visualization tool to display the VSLAM output, such as the robot's estimated pose, the generated map, and feature tracks.

### Example (Conceptual)

Assuming you have Isaac ROS setup within a Docker container and a simulated camera providing image data on a `/image_raw` topic:

```bash
# Inside the Isaac ROS Docker container
ros2 launch isaac_ros_vslam isaac_ros_vslam.launch.py \
    image_topic:=/image_raw \
    odom_topic:=/vslam/odom \
    map_frame:=map \
    odom_frame:=odom \
    base_frame:=base_link
```

This command would launch the VSLAM node, processing image data and publishing odometry (`odom`) and map information. You would then open RViz and add a `TF` display to see the coordinate frames and a `Map` display to visualize the generated map.
