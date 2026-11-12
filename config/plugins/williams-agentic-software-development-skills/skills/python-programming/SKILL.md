---
name: python-programming
description: Instructions for writing computer programs using the Python programming language; use when implementing, refactoring, or reviewing Python code and package APIs.
---

# Python Programming

Instructions for writing computer programs using the Python programming language. Use this skill when implementing, refactoring, or reviewing Python code and package APIs.

- **Expose public functions:** Declare public API functions without a leading underscore to signal that they are part of the external interface (PEP8).
- **Prefix internal functions:** Prefix module-private functions and variables with a single leading underscore to indicate internal implementation details (PEP8).
- **Define inner helpers without underscores:** Format inner helper functions without leading underscores because their visibility is already restricted to their enclosing scope.
- **Expose package APIs via init:** Expose a package subsystem's public API explicitly through `__init__.py` while keeping internal implementation modules private (PEP8).
- **Choose pattern matching versus if statements:** Use match/case statements for equality checks against multiple discrete values (PEP634), and reserve if statements for boolean conditional logic.
