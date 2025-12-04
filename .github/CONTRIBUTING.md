# Contributing to FlowWrite-AI-Writing-Assistant-Browser-Extension

Thank you for your interest in contributing to **FlowWrite-AI-Writing-Assistant-Browser-Extension**! We welcome all contributions, from bug reports and feature requests to code submissions and documentation improvements.

This project adheres to the Apex Technical Authority standards, emphasizing Zero-Defect, High-Velocity, and Future-Proof development. All contributions should align with these principles and the established architecture.

## 1. Code of Conduct

This project has adopted the Contributor Covenant as its Code of Conduct. Please review the [CODE_OF_CONDUCT.md](https://github.com/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension/blob/main/CODE_OF_CONDUCT.md) to understand the expected standards of behavior.

## 2. How to Contribute

### 2.1 Reporting Bugs

If you find a bug, please submit an issue on GitHub. Use the provided bug report template to ensure all necessary information is captured. Be sure to include:

*   A clear, descriptive title.
*   A detailed description of the issue.
*   Steps to reproduce the bug.
*   The expected behavior vs. the actual behavior.
*   Relevant environment details (browser version, OS, extension version if applicable).
*   Screenshots or error logs, if available.

### 2.2 Feature Requests

We encourage you to suggest new features or improvements. Please submit a new issue with the "feature request" label. Clearly describe:

*   The proposed feature.
*   The problem it aims to solve.
*   Any potential benefits or use cases.

### 2.3 Submitting Code Contributions

We welcome your code! Here's the general workflow for submitting contributions:

1.  **Fork the Repository:** Create your own fork of the `chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension` repository.
2.  **Clone Your Fork:** Clone your forked repository to your local machine.
    bash
    git clone https://github.com/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension.git
    cd FlowWrite-AI-Writing-Assistant-Browser-Extension
    
3.  **Set Up Your Development Environment:**
    *   Install Node.js (v20+ recommended).
    *   Install the latest version of [npm](https://www.npmjs.com/get-npm) or [yarn](https://yarnpkg.com/).
    *   Install dependencies:
        bash
        npm install
        # or
        yarn install
        
    *   Refer to the `README.md` or `AGENTS.md` for specific build and linting commands.
4.  **Create a New Branch:** Create a descriptive branch for your changes (e.g., `feature/add-new-suggestion-type`, `fix/incorrect-groq-api-call`).
    bash
    git checkout -b your-branch-name
    
5.  **Make Your Changes:** Implement your feature or fix your bug. Ensure your code follows the project's coding standards and architectural guidelines.
6.  **Test Your Changes:** Run the test suite to ensure your changes haven't introduced regressions.
    bash
    npm run test
    # or
    yarn test
    
    If adding new functionality, write new tests.
7.  **Lint and Format:** Ensure your code adheres to the project's linting and formatting rules.
    bash
    npm run lint
    npm run format
    # or
    yarn lint
    yarn format
    
8.  **Commit Your Changes:** Commit your changes with clear, concise messages.
    bash
    git add .
    git commit -m "feat: Add feature X for Y" 
    # or
    git commit -m "fix: Resolve issue Z in component A"
    
9.  **Push Your Branch:** Push your branch to your fork on GitHub.
    bash
    git push origin your-branch-name
    
10. **Open a Pull Request:** Submit a pull request from your branch to the `main` branch of the `chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension` repository.
    *   **PR Template:** Use the provided pull request template and fill it out completely.
    *   **Description:** Clearly explain the changes, the problem solved, and any relevant context.
    *   **Testing:** Confirm that all tests are passing and that you've added new tests where appropriate.

### 2.4 Architectural Standards

*   **Technology Stack:** This project utilizes **TypeScript** for robust frontend development, **Vite** for fast building, and **TailwindCSS v4** for utility-first styling. For browser extensions, **WXT (Web Extension Toolkit)** is used, ensuring compatibility across various browser extension platforms.
*   **Architecture:** Adheres to **Feature-Sliced Design (FSD)** principles for maintainable and scalable code organization.
*   **Linting & Formatting:** **Biome** is used for extremely fast linting and code formatting. Ensure all code is formatted before committing.
*   **Testing:** **Vitest** is used for unit tests, and **Playwright** is used for end-to-end testing. All new code must be accompanied by relevant tests.
*   **AI Integration:** When interacting with AI models (Groq, Cerebras, Gemini), prioritize modularity, clear API contracts, and robust error handling, with specific attention to privacy and rate-limit awareness.

## 3. Development Guidelines

*   **Follow the Apex Principles:** Adhere to Zero-Defect, High-Velocity, and Future-Proof development.
*   **DRY (Don't Repeat Yourself):** Avoid redundant code. Use abstractions and utilities where appropriate.
*   **SOLID Principles:** Apply SOLID principles to ensure maintainable and extensible code.
*   **YAGNI (You Ain't Gonna Need It):** Do not implement features until they are actually required.
*   **Code Readability:** Write clear, well-commented code. Use meaningful variable and function names.
*   **Security:** Be mindful of security best practices, especially when handling API keys or user data. Refer to the [.github/SECURITY.md](https://github.com/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension/blob/main/.github/SECURITY.md) file for guidelines.

## 4. Pull Request Checklist

*   [ ] My code adheres to the project's coding standards.
*   [ ] I have performed a self-review of my own code.
*   [ ] I have commented my code, particularly in hard-to-understand areas.
*   [ ] I have made corresponding changes to the documentation (if applicable).
*   [ ] My changes generate no new warnings and pass linting and formatting checks.
*   [ ] I have added tests that prove my fix is effective or that my feature works.
*   [ ] All new and existing unit tests pass locally with my changes.
*   [ ] Any dependent components have been updated or are compatible.
*   [ ] I have provided clear descriptions in the commit messages and the PR description.
*   [ ] I have followed the Pull Request Template instructions.

We look forward to your contributions!
