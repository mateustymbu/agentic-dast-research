Agentic DAST Research: Autonomous Security Testing for SPAs
Project Status: Research and Development

Overview
Agentic DAST is an open-source research initiative aimed at solving the "navigation gap" in Dynamic Application Security Testing (DAST) for modern Single Page Applications (SPAs).

Traditional security scanners often fail to crawl deep application states (like authenticated checkout flows) in JavaScript-heavy apps. This framework solves this by using an LLM-driven agent to orchestrate a headless browser (Puppeteer). Instead of random crawling, the agent uses the Screenplay Pattern to navigate semantically (e.g., "login," "add to cart") and reach critical business logic.

Key Features (Research Goals)
Semantic Navigation: The agent parses the DOM to understand user intent ("Click the checkout button") rather than relying on brittle CSS selectors.

Context-Aware Fuzzing: Utilizes LLMs to analyze API schemas and generate valid, context-specific malicious payloads (Semantic Fuzzing) to test for Logic Flaws and IDOR.

Self-Healing: Automatically recovers from UI changes by re-evaluating the page structure during execution.

Architecture
The project leverages a hybrid approach:

Navigation: Puppeteer (Node.js) controlled by an Agentic Loop.

Security Scanning: OWASP ZAP (running in Daemon mode) proxied behind the browser.

Reasoning Core: Large Language Models (OpenAI GPT-4 / Local Models) for decision making and payload generation.

Roadmap
[1] Literature Review & Architecture Design (Current Phase)

[2] Prototype: Basic Semantic Navigation with Puppeteer

[3] Integration: Puppeteer + OWASP ZAP Proxy

[4] Implementation: LLM-based Payload Generation

[5] Evaluation: Benchmark against OWASP Juice Shop

Academic Context
This project is being developed as an undergraduate thesis (TCC) in Computer Engineering. The goal is to produce empirical evidence on the efficacy of LLM-agents in uncovering business logic vulnerabilities compared to traditional DAST scanners.
