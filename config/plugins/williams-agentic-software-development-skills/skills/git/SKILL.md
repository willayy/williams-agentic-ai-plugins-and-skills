---
name: git
description: Instructions for conventional commits, software object scoping, and Git repository operations; use when staging changes, authoring commits, or synchronizing Git repositories.
---

# Git

Instructions for creating conventional commits, scoping changes to individual software objects, and managing Git repositories. Use this skill when staging changes, authoring commits, or synchronizing Git repositories.

- **Limit commits to single software objects:** Scope each commit strictly to changes on exactly one software object (function, method, class, global constant, global variable, configuration file, or documentation file).
- **Format commit headers:** Structure commit messages using the conventional commit format `<type>(scope): <description>` in lowercase imperative mood followed by an optional body.
  - `feat(auth): add verify_token method`
  - `fix(parser): prevent null reference when input is empty`
  - `refactor(models): move user_validator to separate module`
  - `refactor(auth): rename user_token to auth_token`
  - `refactor(cache): swap redis_client with memcached_client`
  - `docs(readme): add installation instructions`
- **Apply standard commit prefixes:** Use `feat` for new software objects, `fix` for broken code, `refactor` for non-breaking code changes, `docs` for documentation, `test` for tests, `chore` for build and config files, and `perf` for performance improvements.
- **Identify broken behavior for fixes:** Apply the `fix` prefix exclusively to code producing unintended or unexpected behavior not documented as accepted.
- **Constrain description verbs:** Begin the description with one of the allowed imperative verbs: `add`, `allow`, `enforce`, `extract`, `move`, `prevent`, `remove`, `rename`, `swap`, or `update`.
- **Synchronize remote branches:** Push commits to the remote branch only after all intended software object changes have been cleanly committed.
- **Preserve repository integrity:** Do not create or write unreviewed artifacts or untracked state modifications during version control operations.
