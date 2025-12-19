# Data Model: AI-Robot Brain Module

This document defines the structure of the AI-Robot Brain module.

## Chapter

A chapter is a single page of content within the module.

-   **Fields:**
    -   `title`: (string) The title of the chapter.
    -   `file_name`: (string) The name of the markdown file for the chapter.
-   **Relationships:**
    -   Belongs to the AI-Robot Brain Module.

## Example Structure

```
- Module 3: The AI-Robot Brain (NVIDIA Isaac™) (short_name: ai-robot-brain-module-3)
  - Chapter 1: Isaac Sim (file_name: 1-isaac-sim.md)
  - Chapter 2: Isaac ROS (file_name: 2-isaac-ros.md)
  - Chapter 3: Nav2 Path Planning (file_name: 3-nav2-path-planning.md)
```
