# Data Model: Vision-Language-Action (VLA) Module

This document defines the structure of the Vision-Language-Action module.

## Chapter

A chapter is a single page of content within the module.

-   **Fields:**
    -   `title`: (string) The title of the chapter.
    -   `file_name`: (string) The name of the markdown file for the chapter.
-   **Relationships:**
    -   Belongs to the VLA Module.

## Example Structure

```
- Module 4: Vision-Language-Action (VLA) (short_name: vla-module-4)
  - Chapter 1: Voice-to-Action with Whisper (file_name: 1-voice-to-action.md)
  - Chapter 2: Cognitive Planning (NL → ROS 2 actions) (file_name: 2-cognitive-planning.md)
  - Chapter 3: Capstone: Autonomous Humanoid (file_name: 3-autonomous-humanoid.md)
```
