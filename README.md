Agentic DAST: Autonomous Security Testing for SPAs
!(https://img.shields.io/badge/Status-Research%20Prototype-blue)

Overview
Agentic DAST is an open-source research initiative aimed at solving the "navigation gap" in Dynamic Application Security Testing (DAST) for modern Single Page Applications (SPAs).

Traditional security scanners often fail to crawl deep application states (like authenticated checkout flows) in JavaScript-heavy apps. This framework solves this by using an LLM-driven agent to orchestrate a headless browser (Puppeteer). Instead of random crawling, the agent uses the Screenplay Pattern to navigate semantically and reach critical business logic.

Key Features (Research Goals)
Semantic Navigation: The agent parses the DOM to understand user intent (e.g., "Find the checkout button") rather than relying on brittle CSS selectors.

Context-Aware Fuzzing: Utilizes LLMs to analyze API schemas and generate valid, context-specific malicious payloads to test for Business Logic Vulnerabilities and IDOR.

Deep State Coverage: Capable of reaching complex application states (e.g., adding items to cart, proceeding to payment) before launching attacks.

Architecture
The project leverages a hybrid approach:

Navigation Module: Puppeteer (Node.js) controlled by an Agentic Loop for precise browser manipulation.

Security Scanner:(https://www.zaproxy.org/) (running in Daemon mode) proxied behind the browser to capture and analyze traffic.

Reasoning Core: Large Language Models (OpenAI GPT-4 / Claude 3.5) for decision making and payload generation.

Roadmap
[1] Literature Review & Architecture Design (Current Phase)

[2] Prototype: Basic Semantic Navigation with Puppeteer

[3] Integration: Puppeteer + OWASP ZAP Proxy

[4] Implementation: LLM-based Payload Generation (Semantic Fuzzing)

[5] Evaluation: Benchmark against OWASP Juice Shop

🎓 Academic Context
This project is being developed as an undergraduate thesis (Capstone Project) in Computer Engineering. The goal is to produce empirical evidence on the efficacy of LLM-agents in uncovering business logic vulnerabilities compared to traditional DAST scanners.
