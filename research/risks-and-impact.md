# AI Coding Agents: Risks, Limitations, and Impact on Developers

## Overview
This document outlines the security risks, reliability limitations, and long-term impact on developers associated with integrating AI coding agents into modern software engineering workflows.

Researcher: Sebastian Gonzalez

---

## 1. Reliability & Security Risks
- **Specific Vulnerability Rates in AI Generation:** According to the Veracode GenAI Code Security Analysis, roughly 44% of tested code-generation tasks introduced a security vulnerability. This finding reflects specific experimental tasks rather than all available commercial agents, commonly introducing flaws such as SQL Injection (CWE-89) and Cross-Site Scripting (CWE-79).
- **Package Hallucination & Supply Chain Risks ("Slop Squatting"):** AI models occasionally generate non-existent package dependencies or library names (package hallucinations). Security research from ReversingLabs demonstrates that attackers monitor these fictional package names to publish malicious libraries on public registries like npm or PyPI. 
- **Codebase Degradation and Technical Debt:** Rapid generation of unverified code risks introducing low-quality, redundant snippets ("slop code") that can increase architectural debt and long-term codebase fragility.
- **Secret & Telemetry Exposure:** Uploading proprietary source code or environment tokens to cloud-hosted AI coding tools introduces data privacy risks if enterprise guardrails or local model hosting are not utilized. 

## 2. Why Human Review and Testing Remain Essential

- **Contextual and Domain Limitations:** AI agents evaluate code using local context windows or specific prompts. They lack deep visibility into overall system architecture, domain-specific compliance requirements, and complex business logic.
- **Widespread Review Requirement:** The Sonar State of Code Survey reports that 95% of surveyed developers spend effort reviewing, testing, and correcting AI-generated code, confirming that manual oversight remains standard practice.
- **Comparative Review Overhead:** Findings from Sonar indicate that AI-assisted pull requests often require higher review effort and code inspection compared to traditional human-written code.
- **Accountability & Legal Liability:** AI models cannot assume legal or financial accountability for security breaches or outage costs. The human engineer remains legally responsible for code deployed to production.
---

## 3. Shifting Responsibilities for Developers

- **Potential Transition Toward Code Auditing:** Developer roles may progressively shift from writing initial boilerplate syntax toward reviewing, auditing, and refactoring agent-generated outputs.
- **Focus on System Architecture and Threat Modeling:** As syntax suggestions become automated, software engineering responsibilities are expected to place greater emphasis on system design, threat modeling, and contract definitions.
- **Prompt Engineering and Agent Orchestration:** Software teams may increasingly require skills in prompt boundary setting, specification writing, and agent workflow orchestration.
- **Elevated Quality Assurance and Edge-Case Analysis:** Human developers remain essential for writing integration tests and identifying edge cases that AI models may overlook.

---

## 4. Supported Facts vs. Future Predictions
| Supported Facts (Current Evidence) | Future Predictions (Industry Trends) |
| :--- | :--- |
| **Tested Vulnerability Rates:** Veracode research shows that roughly 44% of tested code-generation benchmarks introduced security flaws. | **Autonomous PR Workflows:** AI coding agents may eventually handle end-to-end pull requests and bug fixes autonomously. |
| **High Review Participation:** 95% of surveyed developers report spending effort reviewing and fixing AI-generated code (*Sonar Report*). | **Role Evolution for Junior Developers:** Entry-level engineering tasks could transition further toward prompt design, code auditing, and specification testing. |
| **Supply Chain Vulnerabilities:** Attackers actively target package hallucinations on public registries like PyPI and npm (*ReversingLabs Research*). | **Compounding Technical Debt:** Enterprise maintenance overhead could grow if unvetted AI snippets accumulate in production repositories over time. |

---

## 5. Credible Sources & References

1. **Snyk** (Published 2024). *AI Code Generation Security & Quality Analysis*.
URL: [https://snyk.io/blog/ai-code-generation-code-security-quality-benefits-risks-top-tools/](https://snyk.io/blog/ai-code-generation-code-security-quality-benefits-risks-top-tools/)
2. **Veracode** (Punlished: 2024). *GenAI Code Security Analysis*.
URL: [https://www.veracode.com/blog/2026-genai-code-security-report-ai-risk/](https://www.veracode.com/blog/2026-genai-code-security-report-ai-risk/)
3. **SonarSource** (Published 2024). *The State of Code & Developer Survey Report*.
URL: [https://www.sonarsource.com/state-of-code-developer-survey-report.pdf](https://www.sonarsource.com/state-of-code-developer-survey-report.pdf)
4. **Cloud Security Alliance (CSA)** (Published: April 6, 2026). *AI Codegen & Vulnerability Debt Research Note*.
URL: [https://labs.cloudsecurityalliance.org/research/csa-research-note-ai-codegen-vulnerability-debt-20260406-csa/](https://labs.cloudsecurityalliance.org/research/csa-research-note-ai-codegen-vulnerability-debt-20260406-csa/)
5. **Arnica** (Published: 2024). *AI-Generated Code Security Complete Guide*.
URL: [https://www.arnica.io/blog/ai-code-security-complete-guide](https://www.arnica.io/blog/ai-code-security-complete-guide)
6. **ReversingLabs Research** (Published: May 2023). *Luring Developers with Malicious Hallucinated Packages*.
URL: [https://www.reversinglabs.com/blog/ai-package-hallucination-malware-threats](https://www.reversinglabs.com/blog/ai-package-hallucination-malware-threats)
8. **OX Security** (Published: 2024). *AI Code Security Guide*.
URL: [https://www.ox.security/blog/ai-code-security/](https://www.ox.security/blog/ai-code-security/)
