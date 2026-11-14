---
name: skill-rules-creation
description: Instructions for authoring and formatting skills and agent rule files; use when designing, creating, or auditing Antigravity skills or AGENTS.md rule files.
---

# Skill and Rules Creation

Instructions for authoring and formatting skills and agent rule files.
Use this skill when designing, creating, or auditing Antigravity skills or AGENTS.md rule files.

- **Include skill YAML frontmatter:** In skills, include frontmatter matching the directory name.
- **Follow skill naming conventions:** Name skills using lowercase kebab-case matching directory.
- **State invocation triggers:** In skills, specify invocation triggers in frontmatter and intro.
- **Define top-level title:** Begin with a single top-level heading reflecting the scope.
- **Write single-paragraph introduction:** In skills, place one intro paragraph under the title.
- **Specify execution procedure:** Dictate specifically how to perform a task, never what to do.
- **Prevent conflicting instructions:** Never include overlapping or contradicting instructions.
- **Format instructions as list items:** Format instructions as bullet points or enumerated steps.
- **Make bullet points action-oriented:** Formulate instruction bullets as action-oriented rules.
- **Separate action from details:** Use bold text for generic action and description for exacts.
- **Limit instruction length:** Formulate every instruction item as exactly one complete sentence.
- **Omit intermediate skill headers:** Do not use intermediate section headers (`##`) in skills.
- **Indent example items:** Place examples as indented bullet points directly beneath the rule.
