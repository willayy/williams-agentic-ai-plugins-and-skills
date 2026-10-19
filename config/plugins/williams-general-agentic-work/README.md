# General Agentic Work Plugin

A Gemini and Antigravity plugin bundling general agentic workflows, text review, skill creation, and sandbox execution.

## Plugin Rules

- `rules/AGENTS.md`: Plain-text caching rules for agent workflows.

## Bundled Skills

- `ask`: Rules for answering questions by routing dynamically between project resources and internet sources.
- `ask-internet`: Rules for answering questions exclusively using resources and citations from the internet.
- `ask-project`: Rules for answering questions exclusively using resources and citations from the current project directory.
- `explain-issue-and-propose-fix`: Rules for explaining an issue, diagnosing its cause, and proposing a fix.
- `review-text`: Rules for reviewing text for logical, stylistic, typographical, semantic, grammatical, and punctuation errors.
- `sandbox-task`: Rules for executing autonomous tasks strictly confined inside the sandbox environment.
- `skill-creation`: Rules and structural guidelines for creating new skills.
