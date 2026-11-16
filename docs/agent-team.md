# Agent team for Mona's Project Pulse dashboard

This project will use a small specialist team defined under the repository's `.github/agents/` folder, coordinated through GitHub Copilot CLI in a Codespace.

- Planner — Model: Claude Opus 5.5 — researches the repository, identifies dependencies and edge cases, and produces the implementation strategy and file assignments. Definition: `.github/agents/planner.agent.md`.
- Orchestrator — Model: Claude Opus 5.5 — breaks the plan into executable phases, delegates work to the specialist agents, and coordinates execution while keeping file scopes separate. Definition: `.github/agents/orchestrator.agent.md`.
- Coder — Model: GPT-5.5 (copilot) — implements the logic, fixes bugs, and writes the production code needed for the dashboard in the areas assigned by the Orchestrator. Definition: `.github/agents/coder.agent.md`.
- Designer — Model: Gemini 3.7 Flash (copilot) — focuses on UX, accessibility, visual hierarchy, responsive behavior, and the polished Project Pulse dashboard styling. Definition: `.github/agents/designer.agent.md`.

Together, the team will work as a coordinated pipeline: the Planner researches the repo and creates the implementation strategy, the Orchestrator breaks it into phases and delegates work to the right specialist, the Designer shapes the dashboard UX and styling, and the Coder implements and validates the code. The Orchestrator keeps each agent within clear file scopes so the team can work in parallel where possible, then integrates the pieces into a single Project Pulse dashboard in the Copilot CLI Codespace workflow.
