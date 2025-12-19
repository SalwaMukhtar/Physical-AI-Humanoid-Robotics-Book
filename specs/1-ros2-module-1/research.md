# Research: Docusaurus Version and Plugin Policy

**Decision:**
-   **Docusaurus Version:** The project will use the latest stable major version of Docusaurus, which is currently **Docusaurus v3**. We will stay updated with minor and patch releases as they become available.
-   **Plugin Policy:** Third-party plugins should be used sparingly and only after careful consideration. Each plugin must meet the following criteria:
    -   It is actively maintained.
    -   It has a good reputation in the community.
    -   It is genuinely necessary and provides significant value.
    -   It does not introduce unnecessary complexity or dependencies.

**Rationale:**
-   Docusaurus recommends staying on the latest version to benefit from new features, performance improvements, and security patches. There is no official LTS version.
-   A strict plugin policy will help to ensure the long-term stability and maintainability of the project.

**Alternatives considered:**
-   Sticking to a specific minor version of Docusaurus was considered, but this would mean missing out on important updates and is not the recommended approach by the Docusaurus team.
-   Allowing any plugins was considered, but this could lead to a fragile and difficult-to-maintain project in the long run.
