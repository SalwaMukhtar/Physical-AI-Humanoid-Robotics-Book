# Data Model: Book Structure

This document defines the structure of the book, including modules and chapters.

## Module

A module is a top-level container for a set of related chapters.

-   **Fields:**
    -   `title`: (string) The title of the module.
    -   `short_name`: (string) A short name for the module, used in the URL and directory name.
    -   `description`: (string) A brief description of the module.
-   **Relationships:**
    -   Has many Chapters.

## Chapter

A chapter is a single page of content within a module.

-   **Fields:**
    -   `title`: (string) The title of the chapter.
    -   `file_name`: (string) The name of the markdown file for the chapter.
-   **Relationships:**
    -   Belongs to one Module.

## Example Structure

```
- Module 1: The Robotic Nervous System (ROS 2) (short_name: ros2-module-1)
  - Chapter 1: ROS 2 Fundamentals (file_name: 1-ros-fundamentals.md)
  - Chapter 2: Python Agents with rclpy (file_name: 2-python-agents.md)
  - Chapter 3: Humanoid Modeling with URDF (file_name: 3-humanoid-modeling.md)
```
