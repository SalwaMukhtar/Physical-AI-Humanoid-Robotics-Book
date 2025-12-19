# Data Model: Digital Twin Module

This document defines the structure of the Digital Twin module.

## Chapter

A chapter is a single page of content within the module.

-   **Fields:**
    -   `title`: (string) The title of the chapter.
    -   `file_name`: (string) The name of the markdown file for the chapter.
-   **Relationships:**
    -   Belongs to the Digital Twin Module.

## Example Structure

```
- Module 2: The Digital Twin (Gazebo & Unity) (short_name: digital-twin-module-2)
  - Chapter 1: Gazebo Physics Simulation (file_name: 1-gazebo-simulation.md)
  - Chapter 2: Unity for Visualization & Interaction (file_name: 2-unity-visualization.md)
  - Chapter 3: Sensor Simulation (LiDAR, depth, IMU) (file_name: 3-sensor-simulation.md)
```
