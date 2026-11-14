---
name: question-answering
description: Instructions for answering questions by routing dynamically between concise answers and source usage; use when an inquiry may require internal repository files, external web data, or direct answers.
---

# Question Answering

Instructions for answering questions by routing dynamically between direct answers and source usage.
Use this skill when an inquiry may require internal repository files, external web data, or answers.

- **Route information sources:** Route queries to `concise-answers` or source retrieval in `using-source`.
- **Distinguish source passages:** Format quoted source excerpts to remain visibly distinguishable from model-authored commentary using blockquotes.
- **Quote verbatim excerpts:** Reproduce exact, unmodified text segments directly from retrieved sources without paraphrasing quoted passages.
- **Cite authoritative references:** Provide explicit citations referencing exact file paths for internal project resources and canonical URLs for external web sources.
- **Enforce read-only execution:** Resolve inquiries directly without altering, generating, or removing workspace files or configuration variables.
- **Apply presentation formatting:** Render answers using LaTeX equations, structural figures, and descriptive links wherever clarity requires.
