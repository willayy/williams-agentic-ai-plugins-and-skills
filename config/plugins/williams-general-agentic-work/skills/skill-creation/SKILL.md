---
name: skill-creation
description: Rules and structural guidelines for creating new skills.
---

# Skill Creation

Rules and structural guidelines for defining the layout, formatting, and conventions of skills.

- **Frontmatter:** Include YAML frontmatter with `name` matching the skill directory name and a `description` starting with `Rules for ...`.
- **Title:** The skill must begin with a single top-level heading (`# <Title>`) reflecting the skill name without extraneous suffixes (e.g. `Workflow` or `Instructions`).
- **Introduction:** Directly underneath the title, include exactly one paragraph describing the purpose and scope of the skill, following the `Rules for ...` convention, without any intermediate section headers.
- **List formatting:** Format all instructions, rules, and steps as either bullet points (`- **Index:** Description`) or enumerated points (`1. **Index:** Description`) for sequential workflows, with the label bolded before the colon.
- **No intermediate headers:** Do not use intermediate section headers (`##`); integrate all instructions, constraints, and output formats into the formatted list items.
- **Examples:** Only include examples if explicitly requested by the user; omit them entirely if no explicit request was made. When included, format each example as bold text (`**Examples of <topic>:**`) followed directly by a code block (```...```).
