# Security Policy

## Supported Versions

We are committed to maintaining a secure codebase. Currently, we focus our security efforts on the latest stable version of `FlowWrite-AI-Writing-Assistant-Browser-Extension`.

## Reporting a Vulnerability

We welcome security disclosures from security researchers and ethical hackers. To report a security vulnerability, please use the GitHub Security Advisory feature or send an encrypted email to `chirag.dev@example.com` (if available, otherwise indicate preferred secure communication). We kindly ask that you do not disclose any vulnerability publicly until it has been addressed.

When reporting a vulnerability, please provide the following information:

*   **Vulnerability Type:** (e.g., XSS, CSRF, Authentication Bypass, etc.)
*   **Affected Component:** (e.g., specific JavaScript file, browser extension API usage)
*   **Steps to Reproduce:** Detailed, step-by-step instructions to trigger the vulnerability.
*   **Proof of Concept (PoC):** If possible, include code snippets, screenshots, or a video demonstrating the vulnerability.
*   **Impact Assessment:** Describe the potential impact of the vulnerability.
*   **Recommended Mitigation:** Any suggestions for fixing the issue.

We will acknowledge receipt of your vulnerability report within **48 hours** and will provide an estimated timeline for resolution.

## Security Best Practices

*   **Browser Extension Security:** Developers must adhere to the latest security guidelines for browser extensions, including sanitizing all user inputs, restricting unnecessary permissions, and ensuring secure storage of sensitive data (if any).
*   **AI Model Integration:** When interacting with AI models (Groq, Cerebras, Gemini), ensure that API keys are stored securely (e.g., via browser extension storage APIs or environment variables if applicable in development/build) and that input/output is validated to prevent prompt injection or data leakage.
*   **Rate Limiting & Privacy:** Implement robust client-side checks and user notifications for API rate limits. Design all interactions with a privacy-first mindset, minimizing the data sent to external APIs.
*   **Dependencies:** Regularly update dependencies using `uv` and `npm` (or equivalent JavaScript package manager) and scan for known vulnerabilities using tools like `npm audit` or Ruff's security checks.

## Incident Response

Upon receiving a security report, the core development team will:

1.  **Triage:** Assess the severity and impact of the reported vulnerability.
2.  **Investigate:** Attempt to reproduce the vulnerability and identify the root cause.
3.  **Mitigate:** Develop and test a fix for the vulnerability.
4.  **Disclose:** Coordinate public disclosure with the reporter, ideally after a fix is available.
5.  **Deploy:** Release a patched version of the browser extension.

Thank you for helping keep `FlowWrite-AI-Writing-Assistant-Browser-Extension` secure!
