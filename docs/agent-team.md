# Agent team

I will use this custom agent team to build Mona's Project Pulse dashboard:

- **Planner** — Target model: **Claude Opus 5.5 (copilot)**. Researches the repository and documentation, identifies risks and dependencies, and creates an implementation plan; does not write code. Definition: `.github/agents/planner.agent.md`.
- **Designer** — Target model: **Gemini 3.7 Flash (copilot)**. Owns UI/UX, accessibility, information hierarchy, interactions, visual styling, and responsive behavior; for Project Pulse, focuses on polished dashboard styling and clear project/status/priority treatments. Definition: `.github/agents/designer.agent.md`.
- **Coder** — Target model: **GPT-5.5 (copilot)**. Implements assigned code and runnable-app support, keeps behavior clear and testable, and validates changes; for Project Pulse, can configure the app launch to open `app/index.html`. Definition: `.github/agents/coder.agent.md`.
- **Orchestrator** — Target model: **Claude Opus 5.5 (copilot)**. Coordinates the Planner, Coder, and Designer, assigns scoped work in dependency-aware phases, integrates the results, and reports the outcome without implementing the work itself. Definition: `.github/agents/orchestrator.agent.md`.

I am using **GitHub Copilot CLI in a Codespace** to orchestrate the work.
