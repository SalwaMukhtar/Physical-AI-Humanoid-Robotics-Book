---
sidebar_position: 2
---

# Cognitive Planning (NL → ROS 2 actions)

Cognitive planning for robots involves translating high-level natural language commands into a sequence of low-level, executable robot actions. This is a critical step in enabling robots to understand and respond to human instructions in a flexible and intelligent way. Large Language Models (LLMs) are increasingly being used to facilitate this process due to their powerful natural language understanding and generation capabilities.

## The Role of LLMs in Cognitive Planning

LLMs can act as the "brain" of a robot's cognitive planning system by:

1.  **Understanding Natural Language Intent**: LLMs can parse complex sentences, identify the user's goals, and extract relevant entities (objects, locations, states).
2.  **Task Decomposition**: They can break down a high-level task (e.g., "make coffee") into a series of smaller, manageable sub-tasks (e.g., "go to coffee machine", "insert pod", "press button").
3.  **Action Sequencing**: LLMs can determine the logical order of these sub-tasks, considering preconditions and postconditions of each action.
4.  **Parameter Grounding**: They can map abstract concepts in natural language to concrete parameters for robot actions (e.g., "red cup" to a specific object ID or coordinates).
5.  **Reasoning and Adaptation**: With appropriate prompting, LLMs can perform basic reasoning, handle ambiguities, and even suggest alternative plans if the initial one fails or is impossible.

## Translating Natural Language to ROS 2 Actions

The core challenge is to reliably convert the LLM's output into a format that a ROS 2 robot can understand and execute. This typically involves:

1.  **Defining the Robot's Action Space**: Before any planning, the robot's capabilities must be clearly defined. This means listing all available ROS 2 actions, services, and topics, along with their parameters and expected outcomes.
    -   **Example Actions**:
        -   `navigate_to_pose(x, y, theta)`
        -   `pick_object(object_id)`
        -   `place_object(location_id)`
        -   `open_gripper()`
        -   `close_gripper()`
2.  **Prompt Engineering**: Crafting effective prompts for the LLM is crucial. The prompt usually includes:
    -   A clear instruction (the user's command).
    -   The robot's current state (e.g., current location, objects it sees, gripper state).
    -   A list of available actions and their parameters, possibly with examples of their usage.
    -   A request for the LLM to output a sequence of actions in a structured format (e.g., JSON, YAML, or a specific function call format).

### Example Workflow (Conceptual)

**User Command**: "Robot, please pick up the red block and place it on the table."

**1. LLM Prompt Construction**:

```
System: You are a robot assistant. Your available actions are:
- pick_object(object_name)
- place_object(location_name)
- navigate_to_object(object_name)
- navigate_to_location(location_name)

Current state: Robot is at (0,0,0), sees blue_block at (1,1,0), red_block at (2,0,0), table at (3,0,0). Gripper is open.

User: pick up the red block and place it on the table.

Output a JSON array of actions with parameters.
```

**2. LLM Response (Example)**:

```json
[
  {"action": "navigate_to_object", "params": {"object_name": "red_block"}},
  {"action": "pick_object", "params": {"object_name": "red_block"}},
  {"action": "navigate_to_location", "params": {"location_name": "table"}},
  {"action": "place_object", "params": {"location_name": "table"}}
]
```

**3. ROS 2 Action Execution**: A dedicated "Cognitive Planner" ROS 2 node would:
    -   Receive the natural language command.
    -   Query the robot's current state (e.g., via ROS 2 topics/services).
    -   Construct the LLM prompt.
    -   Send the prompt to the LLM (e.g., via an `LLMClient` API call).
    -   Parse the LLM's structured response.
    -   Execute the sequence of ROS 2 actions, using `rclpy`'s ActionClient or ServiceClient interfaces.
    -   Handle feedback from action servers (success/failure) and potentially re-plan if necessary.

This approach allows the robot to infer complex task sequences from simple human instructions, moving towards truly intelligent automation.
