---
name: sandbox-task
description: Rules for executing autonomous tasks strictly confined inside the sandbox environment.
---

# Sandbox Task

Rules for executing autonomous tasks strictly confined inside the sandbox environment.

- **Strict sandboxing:** Never set `BypassSandbox: true` or request permission to bypass the sandbox; operate entirely within local sandbox constraints.
- **Directory confinement:** Confine all created files, project code, temporary scripts, and generated artifacts strictly to the scratch directory.
- **Autonomous execution:** Execute tasks end-to-end without interrupting for intermediate approvals, diagnosing and resolving issues autonomously.
- **Environment verification:** Verify all outcomes directly within the sandbox using tests, linters, or execution checks.
- **Final summary:** Provide a concise summary of the completed work and the absolute paths to all files created in the scratch directory.
