---
sidebar_position: 3
---

# Humanoid Modeling with URDF

This chapter explains the basics of the Unified Robot Description Format (URDF).

URDF is an XML format for representing a robot model. It is commonly used in ROS to describe the physical structure of a robot.

A URDF file consists of a set of links and joints that define the robot's kinematics.

-   **Links**: These are the rigid parts of the robot. Each link has a name and can have visual, collision, and inertial properties.
-   **Joints**: These connect the links together. Each joint has a name, a type (e.g., revolute, prismatic, fixed), a parent link, and a child link.

Here is a very simple example of a URDF file for a two-link arm:

```xml
<?xml version="1.0"?>
<robot name="simple_arm">

  <link name="base_link">
    <visual>
      <geometry>
        <cylinder length="0.6" radius="0.2"/>
      </geometry>
    </visual>
  </link>

  <link name="arm_link">
    <visual>
      <geometry>
        <box size="0.8 0.2 0.2"/>
      </geometry>
    </visual>
  </link>

  <joint name="base_to_arm" type="revolute">
    <parent link="base_link"/>
    <child link="arm_link"/>
    <axis xyz="0 0 1"/>
    <limit effort="1000.0" lower="0.0" upper="0.9" velocity="0.5"/>
  </joint>

</robot>
```
