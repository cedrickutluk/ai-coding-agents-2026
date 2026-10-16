# AI Coding Agents: Risks, Limitations, and Impact on Developers

## Overview
This document outlines the security risks, reliability limitations, and long-term impact on developers associated with integrating AI coding agents into modern software engineering workflows.

Researcher: Sebastian Gonzalez

---

## 1. Reliability & Security Risks
- **Elevated Vulnerability Rate in GenAI Output:** Empirical studies from Synk and Veracode indicate that AI code generators output security vulnerabilities in 35% to 45% of generations. Common Flaws include OWASP Top 10 risks such as SQL Injection (CWE-89), Cross-Site Scripting (CWE-79), and improper input validation.
- **Package Hallucination & Supply Chain Attacks ("Slop Squatting"):** AI models frequently invent non-existent package dependencies or library names (package hallucination). Attackers exploit this behavior by registering these hallucinated package names on public registries like npm or PyPI with embedded malware, tricking developers who install AI-suggested dependencies.
- **Codebase Degradation and "Slop Code":** The rapid generation of unverified code leads to an accumulation of low-quality, redundant, and non-optimized snippets ("slop code"). Over time, this creates severe architectural debt and structural brittleness within enterprise codebases.
- **Secret & Telemetry Exposure:** Uploading proprietary source code, internal API endpoints, or environment tokens to cloud-hosted AI coding assistants risks intellectual property exposure and accidental data leaks if prompts are used for model training. 

## 2. Why Human Review and Testing Remain Essential

- **Contextual and Domain Blind Spots:** AI agents evaluate code using local context windows or specific prompt inputs. They lack deep understanding of complex business logic, domain-specific compliance rules, and high-level system architecture.
- **The verification Dilemma:** While AI drastically accelerates code *generation*, validating code correctness requires deep human analysis. Industry benchmarks show that over 90% of AI-generated Pull Requests require manual refactoring or debugging before meeting production standards.
- **Automated Testing Gaps:** AI agents often produce synthetic unit tests that pass superficial checks ("happy paths") but fail to cover complex edge cases, race conditions, or security boundary conditions. Human engineering is required to design comprehensive integration and fuzz tests.
- **Accountability & Legal Liability:** AI models cannot be held legally or financially liable for security breaches, system outages, or regulatory non-compliance (such as GDPR or SOC2). The human engineer retains ultimate responsibility for production code.
---

## 3. Shifting Responsibilities for Developers

- **Transition from Code Authors to Code Auditors:** Developers spend significantly less time writing boilerplate syntax and more time analyzing, validating, and refactoring agent-generated code. Code auditing has become a core competency.
- **Focus on System Architecture and Threat Modeling:** As syntax generation is automated, software engineers shift their primary focus toward high-level system design, threat modeling, API contract governance, and security guardrails.
- **Prompt Engineering and Agent Orchestration:** Engineers must master structuring technical requirements into clear specifications, defining prompt constraints, and orchestrating multiple AI agents in development pipelines.
- **Elevated Quality Assurance and Edge-Case Analysis:** Developers are tasked with identifying subtle logic flaws, performance bottlenecks, and edge cases that AI models consistently overlook.

---

## 4. Supported Facts vs. Future Predictions
| Supported Facts (Current Evidence) | Future Predictions (Industry Trends) |
| :--- | :--- |
| **High Security Failure Rate:** AI code generators output vulnerable code up to 45% of the time when unreviewed (*Snyk/Veracode Studies*). | **Autonomous End-to-End PRs:** AI agents will autonomously write, test, and submit complete pull requests for minor bugs and feature requests. |
| **Review Overhead Bottleneck:** Developers spend significantly more time reviewing and debugging AI output than writing code from scratch (*SonarSource Survey*). | **Transformation of Entry-Level Roles:** Junior engineering roles will shift from writing basic syntax to AI agent auditing, prompt engineering, and specification testing. |
| **Active Supply Chain Vulnerabilities:** Package hallucination ("Slop squatting") is an actively exploited threat vector targeting public package managers (*ReversingLabs*). | **Compounding Technical Debt Costs:** Enterprise maintenance costs will rise substantially due to unvetted AI code merged into production repositories. |

---

## 5. Credible Sources & References

1. **Snyk GenAI Code Security:** [https://snyk.io/blog/ai-code-generation-code-security-quality-benefits-risks-top-tools/](https://snyk.io/blog/ai-code-generation-code-security-quality-benefits-risks-top-tools/)
2. **Veracode GenAI Security Analysis:** [https://www.veracode.com/blog/2026-genai-code-security-report-ai-risk/](https://www.veracode.com/blog/2026-genai-code-security-report-ai-risk/)

3. **SonarSource State of Code:** [https://www.sonarsource.com/state-of-code-developer-survey-report.pdf](https://www.sonarsource.com/state-of-code-developer-survey-report.pdf)
4. **Cloud Security Alliance (CSA):** [https://labs.cloudsecurityalliance.org/research/csa-research-note-ai-codegen-vulnerability-debt-20260406-csa/](https://labs.cloudsecurityalliance.org/research/csa-research-note-ai-codegen-vulnerability-debt-20260406-csa/)
5. **Arnica AI Code Security Guide:** [https://www.arnica.io/blog/ai-code-security-complete-guide](https://www.arnica.io/blog/ai-code-security-complete-guide)
6. **ReversingLabs Research:** [https://www.reversinglabs.com](https://www.reversinglabs.com)
7. **OX Security Guide:** [https://www.ox.security/blog/ai-code-security/](https://www.ox.security/blog/ai-code-security/)
