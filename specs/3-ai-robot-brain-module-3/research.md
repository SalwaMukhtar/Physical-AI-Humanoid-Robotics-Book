# Research: Hardware Requirements for NVIDIA Isaac Sim and Isaac ROS

**Decision:**
-   **Isaac Sim Hardware:**
    -   **GPU:** NVIDIA RTX series GPU (e.g., RTX 3080, RTX 4090) with substantial VRAM (24GB+ recommended for complex scenes). A high CUDA compute capability is essential.
    -   **CPU:** Intel Core i9 or AMD Ryzen 9 (8+ cores).
    -   **RAM:** 64 GB or more (128 GB+ for large simulations).
    -   **Storage:** 1 TB+ NVMe SSD.
    -   **OS:** Ubuntu 20.04/22.04 LTS recommended.
-   **Isaac ROS Hardware:**
    -   **GPU:** An NVIDIA GPU with CUDA support is required (e.g., NVIDIA Jetson platform for edge deployment or discrete RTX series GPU for development workstations).
    -   **CUDA:** A compatible CUDA version as specified by NVIDIA Isaac ROS documentation.
    -   **ROS 2:** A compatible ROS 2 distribution (e.g., Humble).

**Rationale:**
-   NVIDIA Isaac platforms are highly GPU-accelerated. Specific hardware, particularly NVIDIA GPUs with high VRAM and CUDA support, is paramount for performance and functionality.
-   Highlighting these requirements will ensure readers have the necessary setup to run the examples and understand the concepts.

**Alternatives considered:**
-   Using non-NVIDIA hardware for simulation and AI acceleration is generally not feasible for Isaac Sim and Isaac ROS due to their deep integration with NVIDIA's ecosystem.
-   Omitting hardware requirements could lead to user frustration if their systems are not powerful enough.
