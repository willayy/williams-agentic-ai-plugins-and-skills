---
name: question-answering
description: Instructions for answering questions by routing dynamically between project resources and internet sources; use when an inquiry may require internal repository files, external web data, or a synthesis of both.
---

# Question Answering

Instructions for answering questions by determining whether to retrieve information from project resources, internet sources, or both. Use this skill when an inquiry may require internal repository files, external web data, or a synthesis of both.

- **Route information sources:** Autonomously determine whether resolving an inquiry requires project resources (consulting `project-resources`), external internet data (consulting `internet-sources`), or a synthesis of both.
- **Distinguish source passages:** Format quoted source excerpts to remain visibly distinguishable from model-authored commentary using blockquotes.
- **Quote verbatim excerpts:** Reproduce exact, unmodified text segments directly from retrieved sources without paraphrasing quoted passages.
- **Cite authoritative references:** Provide explicit citations referencing exact file paths for internal project resources and canonical URLs for external web sources.
- **Enforce read-only execution:** Resolve inquiries directly without altering, generating, or removing workspace files or configuration variables.
- **Apply presentation formatting:** Render answers using LaTeX equations, structural figures, and descriptive links wherever clarity requires.
