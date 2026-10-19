---
name: add-commit-push
description: Make several different git adds, commits, and pushes with fitting messages.
---

# Add, Commit, and Push

This skill guides staging, committing, and pushing changed files within the current working directory or any specified path while adhering to Git commit rules.

1. **Stage changes:** Stage changed files (`git add`).
2. **Create commit:** Create a Git commit adhering to the Git commit rules.
3. **Iterate:** Repeat steps 1 and 2 until all current changes are committed.
4. **Push changes:** Push changes to the remote branch (`git push`).
5. **Action constraints:** Do not output or write anything to any file, including both code and natural language.
6. **Response:** Respond with all commit messages in a list ordered by time of creation.
