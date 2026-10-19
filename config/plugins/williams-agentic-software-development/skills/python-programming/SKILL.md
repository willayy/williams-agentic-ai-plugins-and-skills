---
name: python-programming
description: Rules for writing computer programs using the Python programming language.
---

# Python Programming

Rules for writing computer programs using the Python programming language.

- **Public functions:** Functions without a leading underscore represent public API.
- **Private functions:** Prefix module-private functions with a leading underscore (`_`).
- **Inner helpers:** Inner helper functions should be written like public functions since their visibility is limited by default.
- **Module scope:** A module (`.py` file) must handle a single entity or responsibility. Place all functions, classes, and constants that implement that responsibility into the same file, and place unrelated logic into separate modules.
- **Package responsibility:** A package (directory containing `__init__.py`) groups related modules that form a complete subsystem. Expose the subsystem's public API through `__init__.py` and keep internal implementation modules private to the package.
- **Conditional branching:** Use `match`/`case` statements for equality checks where a variable can have multiple discrete values. Use `if` statements for testing the boolean value of other conditional logic.
