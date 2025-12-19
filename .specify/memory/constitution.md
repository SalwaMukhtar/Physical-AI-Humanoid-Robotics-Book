<!--
---
Sync Impact Report
---
Version change: 0.0.0 → 1.0.0
Modified principles:
- PRINCIPLE_1_NAME: "Technical Accuracy"
- PRINCIPLE_2_NAME: "Spec-Driven Development"
- PRINCIPLE_3_NAME: "Clarity for Practitioners"
- PRINCIPLE_4_NAME: "End-to-End Applicability"
Added sections:
- PRINCIPLE_5_NAME: "Grounded RAG Chatbot"
- PRINCIPLE_6_NAME: "Open-Source Deployment"
- Key Standards
- Content Scope
Removed sections: None
Templates requiring updates:
- ✅ .specify/templates/plan-template.md
- ✅ .specify/templates/spec-template.md
- ✅ .specify/templates/tasks-template.md
Follow-up TODOs: None
-->
# Physical AI & Humanoid Robotics Book with Embedded RAG Chatbot Constitution

## Core Principles

### I. Technical Accuracy
All claims must be traceable to authoritative sources, such as official documentation, peer-reviewed papers, and reputable open-source repositories. Citations will follow APA style and be embedded in Markdown. No hallucinated content is permitted.

### II. Spec-Driven Development
Development will be reproducible and driven by specifications. This ensures clarity and consistency throughout the project. All specs must be implemented and reproducible.

### III. Clarity for Practitioners
The content will be written with clarity for AI and Robotics practitioners in mind. There should be a clear separation of theory and implementation.

### IV. End-to-End Applicability
The project aims for end-to-end real-world applicability, demonstrating a full Physical AI pipeline from voice to action.

### V. Grounded RAG Chatbot
The embedded RAG chatbot must provide answers grounded only in the indexed book content. Zero hallucinations are allowed. Chatbot responses must be fully grounded.

### VI. Open-Source Deployment
The project will be open-source and deployed on GitHub Pages.

## Key Standards
- All claims traceable to authoritative sources.
- Sources: official docs, peer-reviewed papers, open-source repos.
- Citations: APA-style / Markdown.
- Code: runnable, documented, reproducible.
- No hallucinated content.

## Content Scope
- ROS 2 (nodes, services, URDF, rclpy)
- Digital twins (Gazebo, Unity, sensors)
- NVIDIA Isaac (Sim, ROS, VSLAM, Nav2)
- Vision-Language-Action (Whisper, LLM planning)
- Capstone: voice-controlled autonomous humanoid

## Governance
- The book must build and deploy successfully.
- All specifications must be implemented and reproducible.
- Chatbot responses must be fully grounded with zero hallucinations.
- The project must demonstrate a full Physical AI pipeline (voice → action).

**Version**: 1.0.0 | **Ratified**: 2025-12-17 | **Last Amended**: 2025-12-17