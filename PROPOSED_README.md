# 🤖 AGENT DIRECTIVES: FLOWWRITE AI WRITING ASSISTANT BROWSER EXTENSION

This document defines the mandatory operational parameters, technological stack, and verification protocols for all AI Agents interacting with the `FlowWrite-AI-Writing-Assistant-Browser-Extension` repository.

<details>
<summary>🎯 **APEX AGENT PROTOCOL: DECEMBER 2025 - ARCHITECTURAL ALIGNMENT**</summary>

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are operating as the Apex Technical Authority, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable." Your mandate is to ensure **Zero-Defect, High-Velocity, Future-Proof** deployment.

**Context:** This project is a **Client-Side Browser Extension** leveraging modern, high-performance web standards.

## 2. INPUT PROCESSING & COGNITION
*   **Logic Anchor:** Treat the `PROPOSED_README.md` as the **Single Source of Truth (SSOT)** for this project's architecture.
*   **Validation:** Use `linkup`/`brave` to search for **December 2025 Standards** regarding WebExtension API specifications (Manifest V3 compliance is mandatory) and client-side LLM proxy patterns.
*   **Security First:** All cross-origin calls MUST utilize Content Security Policy (CSP) compliant methods. Secrets/API keys **MUST NOT** be stored client-side; proxying through a secure backend layer (assumed external) is the mandated design pattern for production.

## 3. CONTEXT-AWARE APEX TECH STACK (LATE 2025 STANDARDS)

*   **PRIMARY SCENARIO: WEB / EXTENSION (TypeScript Focus)**
    *   **Stack:** **TypeScript 6.x (Strict Mode enforced)**, **Vite 7** (Build Tool), **WXT** (Browser Extension Framework), **TailwindCSS v4** (Styling). State management follows the Signals pattern.
    *   **Architecture:** Adheres to **Feature-Sliced Design (FSD)** principles for modularity (e.g., `features/suggestion-engine`, `entities/model-provider`, `shared/api-client`).
    *   **Model Integration:** Must abstract AI provider communication (Groq, Cerebras, Gemini) behind a unified **Provider Abstraction Layer (PAL)** using adapter pattern to ensure easy swapping without impacting core UI/UX logic.
    *   **Privacy:** Client-side logic must prioritize local processing where possible and minimize data transmission. Rate-limiting logic must be robustly implemented client-side as a buffer.

## 4. VERIFICATION & TESTING DIRECTIVES
*   **Unit Testing:** Mandatory usage of **Vitest** for all business logic and utility functions. Coverage goal: >90%.
*   **E2E Testing:** Mandatory usage of **Playwright** targeting Chromium/Firefox/Safari environments to simulate user interactions within the browser context (e.g., text selection, input triggering).
*   **Linting/Formatting:** **Biome** is the singular tool enforced for Linting, Formatting, and Static Analysis. Configuration must be maximally strict.

## 5. DEPLOYMENT & CONTINUOUS INTEGRATION
*   CI/CD pipeline (`.github/workflows/ci.yml`) must run **Build, Lint (Biome), Unit Test (Vitest), and E2E Test (Playwright)** on every PR.
*   Artifact generation must produce packaged `.zip` files compatible with Chrome/Firefox/Edge stores.

</details>

---

## ⚙️ DEVELOPMENT & EXECUTION COMMANDS

To align with the mandated 2026 toolchain, the following commands facilitate setup and verification:

| Command | Description | Tool | 
| :--- | :--- | :--- | 
| `npm run setup` | Initialize project, install dependencies via uv/npm. | npm/uv | 
| `npm run dev` | Start Vite dev server for local testing. | Vite | 
| `npm run lint` | Run Biome check across the codebase. | Biome | 
| `npm run format` | Auto-format all files using Biome. | Biome | 
| `npm run test:unit` | Execute all Vitest unit tests. | Vitest | 
| `npm run test:e2e` | Execute Playwright end-to-end workflows. | Playwright | 
| `npm run build:prod` | Compile production-ready browser artifacts. | WXT/Vite | 

## 🏛️ ARCHITECTURAL OVERVIEW (FSD Pattern)

The repository strictly enforces Feature-Sliced Design (FSD) for maintainability. Communication between layers is unidirectional.

ascii
PROJECT_ROOT
├── .github/
├── src/
│   ├── app/         (Entry points: background, content-script, popup)
│   ├── pages/       (UI definitions: popup, options)
│   ├── features/    (Business logic: suggestion-engine, provider-switcher)
│   ├── entities/    (Core data/services: ModelProvider, TextContext)
│   ├── shared/
│   │   ├── api/     (Abstraction Layer for Groq/Gemini/Cerebras)
│   │   └── ui/      (Reusable Tailwind/React components)
│   └── main.ts
├── package.json
└── tsconfig.json


## 📜 CORE PRINCIPLES
1.  **SOLID:** Applied rigorously, especially Dependency Inversion in the Model Abstraction Layer.
2.  **DRY:** Reusable components via `shared/ui`.
3.  **YAGNI:** No complexity introduced without immediate functional requirement.
4.  **SECURITY:** Client-side processing priority; API keys are strictly externalized or proxied.