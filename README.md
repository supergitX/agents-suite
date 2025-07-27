## supergit: AI-Powered Git Workflow Enhancement

supergit is a suite of AI agents designed to seamlessly integrate into any codebase and enhance the capabilities of your Git workflow. By harnessing the power of AI agents in software development and production, supergit aims to transform the way teams work with Git.
<img width="1572" height="828" alt="image" src="https://github.com/user-attachments/assets/94403da4-c62e-4bb2-bcfa-8b23b43b0e4d" />

### <img width="1642" height="909" alt="image" src="https://github.com/user-attachments/assets/5f8e6d08-6ecf-4806-9ce8-875f25d57e5a" />
supergit offers several key features to streamline your development process:

* **Automated Code Generation and Error Fixing:** Automates the creation of code and fixes errors.
* **High-Quality Code with Automated Reviews:** Ensures code quality through automated reviews.
* **Easy Testing with Auto-Generated Test Cases:** Facilitates testing by automatically generating test cases.
* **Detailed Project Documentation:** Creates comprehensive documentation for your project.


### <img width="1347" height="790" alt="image" src="https://github.com/user-attachments/assets/bc00cf35-3cc5-4fd1-a93d-930714e7d380" />

The core concept of supergit relies on the application of large language models (LLMs) to understand and debug code, and to interact with available tools.

* **Large Language Models (LLMs):** Leverages LLMs for code understanding, debugging, and tool interaction.
* **Modularity:** All supergit agents can work independently or together, allowing users to customize functionality.
* **Agents Pipeline:** Agents can be used to set up custom pipeline automations using GitHub Actions workflows.
* **Chatbot for Developers:** Automatically accesses the codebase and prepares context for conversations with developers.
* **Customizability:** Agent behavior can be customized to client requirements.
* **Privacy and Security:** Adaptable to work with local LLM deployments to ensure organizational privacy and security.

### <img width="1291" height="790" alt="image" src="https://github.com/user-attachments/assets/ed8cf6ae-92ca-435c-92b4-e4b47ecdb8c3" />


supergit includes a suite of specialized AI agents:

* **Generator:** This agent generates code directly in the workspace and pushes the file to the repository branch.
* **Tester:** The code tester agent checks committed or issued code for errors.
* **Reviewer:** The code reviewer agent reviews given code, makes corrections, and pushes them back to the repository branch.
* **Critique:** The code critique agent examines all code in a specified path and provides output with comments indicating lines containing errors.
* **Doc-Keeper:** This agent automatically creates documentation and runbooks for the entire repository when triggered.

### <img width="1266" height="736" alt="image" src="https://github.com/user-attachments/assets/c351e377-3da7-4cce-b2b8-e6cf215e0837" />


### Workflow with `workflow.yaml` (Conceptual)

While a specific `workflow.yaml` file is not provided in the document, based on the "Agents Pipeline" strength and the description of the individual agents, a conceptual workflow would involve:

1.  **Triggering Agents:** GitHub Actions workflows would likely be used to trigger the supergit agents. For example, a push to a branch could trigger the `generator` or `tester` agents.
2.  **Automated Code Generation/Testing/Review:**
    * A `workflow.yaml` could be configured to automatically run the `generator` agent upon a specific event (e.g., creating a new feature branch) to scaffold initial code.
    * Upon a pull request or commit, the `tester` agent could be invoked to run tests and report errors.
    * The `reviewer` agent could be integrated into the pull request review process to provide automated code corrections.
3.  **Documentation and Error Reporting:**
    * The `doc-keeper` agent could be scheduled to run periodically or upon major releases to update project documentation.
    * The `critique` agent could be used as part of a pre-commit hook or a separate workflow to provide immediate feedback on code quality and potential errors.
4.  **Integration with Git Operations:** The agents are designed to interact directly with Git, pushing changes back to the repository branches as needed (e.g., `generator`, `reviewer` agents).

This modular design, combined with GitHub Actions, allows users to create customized automation pipelines to fit their specific development needs.

For more details, visit the demo setup repositories at [supergitX GitHub repository](https://github.com/supergitX).
