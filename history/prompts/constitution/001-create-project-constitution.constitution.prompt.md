---
id: 001
title: Create Project Constitution
stage: constitution
date: 2025-12-17
surface: agent
model: gemini-pro
feature: none
branch: main
user: san
command: /sp.constitution
labels: ["constitution", "project-setup"]
links:
  spec: null
  ticket: null
  adr: null
  pr: null
files:
  - .specify/memory/constitution.md
  - .specify/templates/plan-template.md
tests:
  - none
---

## Prompt

/sp.constitution Project:Physical AI & Humanoid Robotics Book with Embedded RAG ChatbotDescription:Create a technical book on Physical AI and Embodied Intelligence using Docusaurus, Spec-Kit Plus, and Claude Code. Deploy to GitHub Pages and embed a RAG chatbot that answers questions strictly from book content, including user-selected text.Core principles:- Technical accuracy from official docs and primary sources- Spec-driven, reproducible development- Clarity for AI/Robotics practitioners- End-to-end real-world applicabilityKey standards:- All claims traceable to authoritative sources- Sources: official docs, peer-reviewed papers, open-source repos- Citations: APA-style / Markdown- Code: runnable, documented, reproducible- No hallucinated contentContent scope:- ROS 2 (nodes, services, URDF, rclpy)- Digital twins (Gazebo, Unity, sensors)- NVIDIA Isaac (Sim, ROS, VSLAM, Nav2)- Vision-Language-Action (Whisper, LLM planning)- Capstone: voice-controlled autonomous humanoidRAG chatbot:- Embedded in Docusaurus- OpenAI Agents/ChatKit, FastAPI- Neon Serverless Postgres, Qdrant Cloud- Answers grounded only in indexed book contentConstraints:- Open-source, GitHub Pages deployment- Clear separation of theory vs implementationSuccess criteria:- Book builds and deploys successfully- All specs implemented and reproducible- Chatbot responses fully grounded, zero hallucinations- Demonstrates full Physical AI pipeline (voice → action)

## Response snapshot

I have successfully created the project constitution and updated the plan template to reflect the new principles.

## Outcome

- ✅ Impact: Created the project constitution and updated the plan template.
- 🧪 Tests: No tests were run.
- 📁 Files: 2 files modified.
- 🔁 Next prompts: none
- 🧠 Reflection: The constitution was created successfully based on the user's input.

## Evaluation notes (flywheel)

- Failure modes observed: none
- Graders run and results (PASS/FAIL): PASS
- Prompt variant (if applicable): null
- Next experiment (none): none
