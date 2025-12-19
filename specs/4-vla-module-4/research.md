# Research: LLMs and Whisper for ROS 2 Integration

**Decision:**
-   **Whisper Version/Integration:** The module will demonstrate integration with OpenAI Whisper, focusing on a Python-based approach within a ROS 2 node. We will assume a `whisper_ros` package, subscribing to audio and publishing text. The plan will mention using ROS 2 parameters for model size and language.
-   **LLM for Cognitive Planning:** The module will conceptually discuss integrating LLMs for cognitive planning. Given the rapid evolution of LLMs, instead of recommending a specific model version, the plan will focus on the *principles* of integration:
    -   Using an `LLMClient` or similar abstraction for interaction.
    -   Formulating prompts that include robot state and available actions.
    -   Parsing LLM responses into structured ROS 2 commands.
    -   The importance of defining a clear action space for the robot.
    -   The role of a "cognitive planner" node to orchestrate these interactions.

**Rationale:**
-   Whisper integration is relatively straightforward via its Python API and can be easily wrapped in a ROS 2 node.
-   Due to the dynamic nature of LLM development, focusing on a specific model version for cognitive planning could quickly lead to outdated content. Instead, emphasizing the architectural patterns and principles for LLM integration will provide more enduring value to the reader.
-   The plan will recommend that the reader can choose their preferred LLM, whether local or API-based, as long as it can take structured prompts and return structured responses suitable for conversion to ROS 2 actions.

**Alternatives considered:**
-   Specifying a concrete LLM version: Rejected due to the fast-changing landscape of LLMs and potential for rapid obsolescence.
-   Ignoring specific Whisper details: Rejected, as Whisper is a concrete tool mentioned in the module description.
