# Bug Report

Thank you for taking the time to report a bug. Please provide as much detail as possible to help us diagnose and fix the issue.

**IMPORTANT:** Before reporting, please check the [Issue Tracker](https://github.com/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension/issues) to see if this bug has already been reported.

## 1. Bug Description

A clear and concise description of the bug. What did you expect to happen, and what actually happened?

*   **Expected Behavior:**
*   **Actual Behavior:**

## 2. Steps to Reproduce

Please provide a step-by-step guide to reproduce the bug. Include any relevant input data or specific actions.

1.  Go to `[URL or context]`
2.  Perform `[Action 1]`
3.  Perform `[Action 2]`
4.  Observe `[Unexpected outcome]`

## 3. Environment Details

*   **Browser:** (e.g., Chrome 120.0.6099.109, Firefox 115.0.2)
*   **Operating System:** (e.g., Windows 11, macOS Sonoma 14.2.1, Linux Ubuntu 22.04)
*   **Extension Version:** (If applicable, check `chrome://extensions` or similar)
*   **AI Model(s) Used:** (e.g., Groq, Gemini, Cerebras)
*   **Other Relevant Information:** (e.g., specific website, other extensions enabled, account type)

## 4. Screenshots/Recordings

If possible, please attach screenshots or a screen recording that clearly illustrates the bug.

## 5. Additional Context

Any other information that might be helpful. This could include logs, error messages, or your thoughts on why the bug might be occurring.

---

---

**AI Agent Directives & Technical Context:**

This section is for developer reference and ensures alignment with the project's core architecture and tooling. It is automatically updated and should not be manually edited by users filing issues.

<details>
<summary>Apex Technical Authority Directives (Project: FlowWrite-AI-Writing-Assistant-Browser-Extension)</summary>

### 1. Identity & Prime Directive

*   **Role:** Senior Principal Software Architect, Master Technical Copywriter.
*   **Experience:** 40+ years elite industry.
*   **Standards:** FAANG-level, "Managing the Unmanageable", "Zero-Defect, High-Velocity, Future-Proof."
*   **Output:** EXECUTION-ONLY.

### 2. Environment & Stack (Late 2025 / 2026 Standards)

*   **Primary Type:** WEB / APP / EXTENSION (TypeScript).
*   **Framework:** Vite 7 (Rolldown), Tauri v2.x (for potential desktop builds).
*   **Language:** TypeScript 6.x (Strict Mode).
*   **UI:** TailwindCSS v4, Signals (Standardized).
*   **Testing:** Biome (Lint/Format), Vitest (Unit), Playwright (E2E).
*   **Architecture:** Feature-Sliced Design (FSD).

### 3. AI Integration (FlowWrite Specific)

*   **Models:** Groq, Cerebras, Gemini.
*   **Client-Side Focus:** Prioritize privacy, rate-limit awareness, and efficient API calls from the browser extension.
*   **API Layer:** Abstract AI model interactions behind a robust service layer.

### 4. Core Principles & Verification

*   **SOLID:** Ensure adherence to Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion principles.
*   **DRY:** Avoid repeating code.
*   **YAGNI:** You Ain't Gonna Need It - build only what is necessary.
*   **Verification:** All code changes must pass automated CI checks (linting, testing, build).

### 5. Key Commands (Development Reference)

*   **Install Dependencies:** `uv pip sync` (or `npm install` if Node.js dependencies exist)
*   **Lint & Format:** `biome check --apply` or `ruff check --fix`
*   **Run Tests (Unit):** `vitest run`
*   **Run Tests (E2E):** `playwright test`
*   **Build Extension:** `vite build`

### 6. Repository & Contribution Standards

*   **Repo URL:** `https://github.com/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension`
*   **License:** CC BY-NC 4.0
*   **Contributing:** See `.github/CONTRIBUTING.md`
*   **CI/CD:** `.github/workflows/ci.yml`

</details>
