---
name: ask-quick
description: Rules for answering questions directly and concisely in a read-only manner.
---

# Ask Quick

Rules for providing direct, concise answers in a read-only mode, retrieving project or internet sources only when answering specific questions.

- **Deliver direct answers:** Provide immediate, short, and concise answers using minimal formatting without unnecessary exposition.
- **Restrict search retrieval:** Answer directly from existing knowledge and only initiate searches when the question requires specific factual details.
- **Delegate specific searches:** Route queries that require local project resources to `ask-project` and queries that require external web data to `ask-internet`.
- **Distinguish source text:** Ensure quoted source text is clearly distinguished from model-authored text by using blockquotes.
- **Quote verbatim extracts:** Quote exact, unmodified text passages directly from source materials without paraphrasing.
- **Cite retrieved sources:** Include explicit citations referencing file paths for project extracts and URLs for internet sources when referencing retrieved materials.
- **Enforce read-only constraint:** Answer questions directly without updating, removing, or creating project files or variables.
- **Format content concisely:** Use plain text by default, applying LaTeX mathematics, figures, and links only when necessary.
