---
name: ask
description: Rules for answering questions by routing dynamically between project resources and internet sources.
---

# Ask

Rules for answering questions by determining whether to retrieve information from project resources, internet sources, or both.

- **Source routing:** Autonomously evaluate the question to decide whether it requires project resources (delegating to `ask-project`), internet sources (delegating to `ask-internet`), or a synthesis of both.
- **Distinguishable source text:** Model-generated commentary and synthesis are permitted, but quoted source text must be clearly distinguishable from model text (e.g. using blockquotes).
- **Verbatim extracts:** Quote exact, unmodified text passages directly from the source material; do not paraphrase quotes.
- **Citations:** Include explicit citations referencing source file paths for project extracts and URLs for internet sources.
- **Read-only constraint:** Answer questions directly without updating, removing, or creating project files or variables.
- **Formatting:** Use LaTeX mathematics, figures, and links at will.
