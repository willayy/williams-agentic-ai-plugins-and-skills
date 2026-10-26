---
name: skill-creation
description: Rules and structural guidelines for creating new skills.
---

# Skill Creation

Rules and structural guidelines for defining the layout, formatting, and conventions of skills.

- **Include YAML frontmatter:** Include YAML frontmatter with `name` matching the skill directory name and a `description` starting with `Rules for ...`.
- **Define top-level title:** The skill must begin with a single top-level heading (`# <Title>`) reflecting the skill name without extraneous suffixes (e.g. `Workflow` or `Instructions`).
- **Write single-paragraph introduction:** Directly underneath the title, include exactly one paragraph describing the purpose and scope of the skill, following the `Rules for ...` convention, without any intermediate section headers.
- **Format instructions as list items:** Format all instructions, rules, and steps as either bullet points (`- **Action label:** Description`) or enumerated points (`1. **Action label:** Description`) for sequential workflows, with the label bolded before the colon.
- **Make bullet points action-oriented:** Bullet points should be action-oriented, either do's or don'ts.
- **Separate generic action from specific details:** Use the bold header text to address the generic action and the description text to provide the exacts.
- **Limit description:** Formulate every bullet point or enumerated item as exactly one complete sentence.
- **Omit intermediate section headers:** Do not use intermediate section headers (`##`) unless grouping instructions into distinct categories; integrate all instructions, constraints, and output formats into the formatted list items.
- **Place examples under corresponding sections:** Include examples only when explicitly requested by the user, placed directly under their corresponding section and formatted as bold text (`**Examples of <topic>:**`) followed directly by a code block (```...```).
