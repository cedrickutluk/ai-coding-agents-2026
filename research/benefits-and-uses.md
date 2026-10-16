# AI Coding Agents: Benefits and Practical Uses

Researcher: Wumaier Kutelike
Related issue: #2
Status: Research in progress

## Current Event

On June 30, 2026, GitHub announced a deeper integration of GitHub Copilot into JetBrains AI Assistant. Developers can select Copilot directly from the agent picker and choose supported models and reasoning depth.

According to GitHub, the agent can work through multistep tasks, examine a project, propose changes, run commands, and iterate with the developer.

This event illustrates how coding tools are expanding beyond code suggestions toward carrying out development tasks inside an IDE.

Source: https://github.blog/changelog/2026-06-30-copilot-agent-is-now-available-in-jetbrains-ai-assistant/

## What Are AI Coding Agents?

For this presentation, an AI coding agent means an AI tool that can use project context and tools to carry out several steps toward a development goal. In the Copilot example, this includes proposing changes and running commands.

These are capabilities described by the vendor, rather than independent evidence that every task becomes faster or more accurate.
## Practical Uses

The following is an illustrative workflow based on the capabilities in GitHub's June 30 announcement, not an experiment we performed:

A developer asks the agent to help fix a small bug. The agent examines the project, proposes changes, runs relevant commands, and iterates with the developer. The developer checks whether the result actually solves the problem.

Other Copilot experiences have related uses. GitHub's documentation lists targeted refactoring, additional tests, and documentation updates as intended uses of the Copilot cloud agent. These are separate from the JetBrains integration and should not be treated as identical products.

## Potential Benefits

Our interpretation of the documented capabilities:

- Delegating several steps may reduce repetitive manual work.
- Working inside the IDE may reduce switching between tools.
- Proposed changes can give developers a starting point to inspect and improve.

These are potential benefits, not measured results from our team. Our sources do not establish a guaranteed speed improvement.

## Limitations

GitHub advises users to carefully review and test generated code. Output may be incorrect or insecure.

The value of an agent depends on the task, available context, and the effort needed to review and correct its work. Human developers remain responsible for deciding whether changes are suitable.

## Sources

### 1. Current-event announcement

- Title: Copilot Agent is now available in JetBrains AI Assistant
- Publisher: GitHub Changelog
- Publication date: June 30, 2026
- URL: https://github.blog/changelog/2026-06-30-copilot-agent-is-now-available-in-jetbrains-ai-assistant/
- Key finding: Copilot became a native option in the agent picker, with model selection and multistep task capabilities.
- Evidence type: Vendor announcement; supports feature descriptions, not independent productivity claims.

### 2. Capabilities and responsible use

- Title: Application card: GitHub Copilot Agents
- Publisher: GitHub Docs
- Publication date: Not displayed; living documentation
- Accessed: October 14, 2026
- URL: https://docs.github.com/en/copilot/responsible-use/agents
- Key finding: Different Copilot experiences have different capabilities and environments. Generated code requires human review and testing.
- Evidence type: Vendor documentation; not an independent evaluation.
