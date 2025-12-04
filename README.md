# FlowWrite-AI-Writing-Assistant-Browser-Extension

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension/ci.yml?style=flat-square)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension?style=flat-square)](https://codecov.io/gh/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue?style=flat-square)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension?style=flat-square)](https://github.com/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension)

| Stack | Linter | Testing |
| :---: | :---: | :---: |
| TypeScript 6.x | Ruff/Biome | Vitest/Playwright |

<p align="center">
  <a href="https://github.com/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension" target="_blank">
    <img src="https://img.shields.io/badge/Star%20%E2%AD%90%20this%20Repo-brightgreen?style=flat-square" alt="Star this Repo"/>
  </a>
</p>

---

FlowWrite is a cutting-edge, privacy-aware browser extension providing real-time, context-sensitive writing suggestions powered by top-tier Large Language Models (LLMs). It seamlessly integrates Groq, Cerebras, and Gemini endpoints to enhance professional and casual communication across all web interfaces.

This project adheres to the **Apex Technical Authority Standard (December 2025)**, emphasizing strict typing, performance optimization via Vite 7, and robust end-to-end testing using Playwright.

## 🏛️ Architecture Overview

The extension utilizes a **Feature-Sliced Design (FSD)** architecture layered over a TypeScript core, ensuring maximum modularity, testability, and future maintainability within the constrained environment of a browser extension.

mermaid
graph TD
    subgraph Browser Environment
        A[Content Script / DOM Listener] --> B(Client-Side Logic / State Mgmt)
    end
    subgraph Extension Core (Service Worker)
        B --> C{API Router / Endpoint Manager}
        C --> D[LLM Provider Abstraction Layer]
        D -- Groq --> E1[Groq API Adapter]
        D -- Gemini --> E2[Gemini API Adapter]
        D -- Cerebras --> E3[Cerebras API Adapter]
    end
    D --> F[Rate Limit & Privacy Guard Module]
    F --> G[Payload Formatting & Response Handling]
    G --> B

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style D fill:#ccf,stroke:#333,stroke-width:2px


## 📚 Table of Contents

1.  [FlowWrite-AI-Writing-Assistant-Browser-Extension](#flowwrite-ai-writing-assistant-browser-extension)
2.  [Architecture Overview](#-%F0%9F%93%84-architecture-overview)
3.  [Table of Contents](#-%F0%9F%93%9A-table-of-contents)
4.  [Core Features](#-%E2%9C%85-core-features)
5.  [Technology Stack (2026 Standard)](#-%F0%9F%92%BB-technology-stack-2026-standard)
6.  [Development & Setup](#-%E2%9C%8F%EF%B8%8F-development--setup)
7.  [Contributing Guidelines](#-%F0%9F%91%8B-contributing-guidelines)
8.  [Security Policy](#-%F0%9F%94%92-security-policy)

## ✅ Core Features

*   **Real-Time Contextual Suggestion:** Provides in-line rewriting, tone adjustment, and expansion based on the currently focused text area.
*   **Multi-LLM Support:** Configurable selection between Groq (Speed), Gemini (Versatility), and Cerebras (Emerging Performance).
*   **Privacy-First Routing:** Client-side filtering and anonymization before sending prompts to external APIs, respecting user privacy mandates.
*   **Dynamic Rate Limiting:** Implements intelligent backoff and queuing to gracefully handle API rate constraints without user interruption.
*   **Strict Typing:** Built entirely in TypeScript with the highest possible `tsconfig.json` compiler options.

## 💻 Technology Stack (2026 Standard)

*   **Frontend/Extension Core:** TypeScript 6.x, Vite 7, Rollup 4
*   **Styling:** TailwindCSS v4 (JIT Compiler)
*   **Testing:** Vitest (Unit/Integration), Playwright (E2E Workflow Simulation)
*   **Linting/Formatting:** Ruff (Linter) and Biome (Formatter) for maximum velocity.
*   **Manifest:** Manifest V3 Compliant.

## 🛠️ Development & Setup

Follow these steps to establish the local development environment compliant with Apex standards.

1.  **Clone Repository:**
    bash
    git clone https://github.com/chirag127/FlowWrite-AI-Writing-Assistant-Browser-Extension.git
    cd FlowWrite-AI-Writing-Assistant-Browser-Extension
    

2.  **Initialize Environment (using uv):**
    *Note: While this is a JS project, we follow the Apex mandate of using modern tooling where applicable for dependency isolation. For JS dependency management, we use npm/yarn, but maintain the configuration philosophy.* 
    bash
    npm install
    

3.  **Execution & Verification:**

| Script | Description |
| :--- | :--- |
| `npm run dev` | Compiles the extension in watch mode (HMR enabled). |
| `npm run build` | Production build of the extension artifacts. |
| `npm run lint` | Runs Ruff/Biome checks across the codebase. |
| `npm run test:unit` | Executes Vitest unit and integration tests. |
| `npm run test:e2e` | Runs Playwright tests against a simulated browser environment. |

### Architectural Principles Enforced

*   **SOLID:** Applied rigorously, especially Dependency Inversion in the API Abstraction Layer.
*   **DRY:** Logic for prompt engineering and error serialization is centralized.
*   **YAGNI:** Features are implemented only when immediately required; speculation is avoided.

<details>
<summary><strong>🤖 AI Agent Directives (APEX_AGENT_V3.1)</strong></summary>

# AGENT INSTRUCTION SET: FLOWWRITE-AI-ASSISTANT

## 1. CONTEXT AND PURPOSE
This repository contains the source code for `FlowWrite-AI-Writing-Assistant-Browser-Extension`. The primary objective is to deliver sub-second, context-aware writing assistance using external LLM APIs (Groq, Gemini, Cerebras) while strictly managing client-side privacy boundaries.

## 2. TECHNICAL STACK MANDATE (BROWSER EXTENSION / FRONTEND)
*   **Language:** TypeScript 6.x (Strict Mode enforced).
*   **Build Tool:** Vite 7 (Leveraging native ES Modules).
*   **Testing Frameworks:** Vitest for unit/integration; Playwright for E2E workflow validation.
*   **Styling:** TailwindCSS v4.
*   **Architecture Pattern:** Feature-Sliced Design (FSD). Structure must separate `app`, `pages` (conceptual), `widgets`, `features`, `entities`, `shared` layers.

## 3. ARCHITECTURAL & CODE VERIFICATION
*   **Dependency Management:** All external API calls must pass through the `LLM Provider Abstraction Layer`. Adapters must implement a standardized `ICompletionRequest` interface.
*   **Security Checkpoint:** All sensitive keys (if any stored client-side, though preferably derived via secure mechanisms) must be obfuscated or handled via secure environment configuration during build.
*   **API Contract Enforcement:** Verify that the `Rate Limit & Privacy Guard Module` correctly serializes requests, injecting necessary headers without exposing raw API keys within the Content Script execution context.
*   **Privacy Audit:** Confirm that DOM scraping for context is minimal and context is sanitized before transmission.

## 4. VERIFICATION COMMANDS
To ensure alignment with the Apex standard, execute the following:

bash
# Verify Linting and Formatting Compliance
npm run lint

# Run Unit/Integration Test Suite
npm run test:unit

# Execute Full E2E Browser Simulation
npm run test:e2e


</details>

## 🤝 Contributing Guidelines

Please refer to the official [CONTRIBUTING.md](./.github/CONTRIBUTING.md) file for contribution standards, branching strategy (feature-gated development), and submission requirements.

## 🔒 Security Policy

We take security seriously. Details on reporting vulnerabilities and our security audit process can be found in the [SECURITY.md](./.github/SECURITY.md) file.

## ⚖️ License

This project is distributed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See the [LICENSE](./LICENSE) file for more details.