---
name: python-programming
description: Rules for writing computer programs using the Python programming language.
---

# Python Programming

Rules for writing computer programs using the Python programming language.

- **Expose public functions:** Declare public API functions without a leading underscore to signal that they are part of the external interface (PEP8).
- **Prefix internal functions:** Prefix module-private functions and variables with a single leading underscore to indicate internal implementation details (PEP8).
- **Define inner helpers without underscores:** Format inner helper functions without leading underscores because their visibility is already restricted to their enclosing scope.
- **Scope modules to a single responsibility:** Confine each module (.py file) to a single entity or responsibility, containing all functions, classes, and constants needed to implement that concern (PEP8).
- **Colocate cohesive code:** Locate code, types, and helper utilities that operate together in the same module or directory to keep related logic colocated (PEP20).
- **Expose package APIs via init:** Expose a package subsystem's public API explicitly through __init__.py while keeping internal implementation modules private (PEP8).
- **Branch conditionally using pattern matching:** Use match/case statements for equality checks against multiple discrete values (PEP634), and reserve if statements for boolean conditional logic.
