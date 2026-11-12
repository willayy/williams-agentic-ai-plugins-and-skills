---
name: skill-creation
description: Instructions for defining the layout, formatting, and conventions of skills; use when designing, authoring, or auditing Antigravity skills.
---

# Skill Creation

Instructions for defining the layout, formatting, and conventions of skills. Use this skill when designing, authoring, or auditing Antigravity skills.

- **Include YAML frontmatter:** Include YAML frontmatter with `name` matching the skill directory name and a `description` starting with `Instructions for...`.
- **State invocation trigger:** Specify clearly in both the frontmatter description and introductory paragraph when the skill should be invoked.
- **Define top-level title:** The skill must begin with a single top-level heading (`# <Title>`) reflecting the skill name without extraneous suffixes (e.g. `Workflow` or `Instructions`).
- **Write single-paragraph introduction:** Directly underneath the title, include exactly one paragraph describing the purpose and scope of the skill, following the `Instructions for...` convention, without any intermediate section headers.
- **Format instructions as list items:** Format all instructions as either bullet points (`- **Action label:** Description`) or enumerated points (`1. **Action label:** Description`) for sequential workflows, with the label bolded before the colon.
- **Make bullet points action-oriented:** Instruction bullet points should be action-oriented, either do's or don'ts.
- **Separate generic action from specific details:** Use the bold header text to address the generic action and the description text to provide the exacts.
- **Limit description:** Formulate every bullet point or enumerated item as exactly one complete sentence.
- **Omit intermediate section headers:** Do not use intermediate section headers (`##`).
- **Place examples as indented bullet points:** Place examples as an indented bullet point of the point it gives an example of.
