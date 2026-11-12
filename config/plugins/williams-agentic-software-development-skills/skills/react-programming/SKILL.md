---
name: react-programming
description: Instructions for writing computer programs using the React JavaScript framework; use when designing, structuring, or implementing React components and UI state.
---

# React Programming

Instructions for writing computer programs using the React JavaScript framework. Use this skill when designing, structuring, or implementing React components and UI state.

- **Enforce MVVM architecture:** Separate concerns by encapsulating domain business logic in the Model, managing UI state and view dynamics in the View-Model, and restricting the View strictly to visual rendering.
- **Inject view-model dependencies:** Declare the View-Model function in the same module as the View component and inject it into the View as a parameter or prop.
- **Favor component composition:** Compose reusable component hierarchies using `props` and `children` rather than redeclaring behavior across component variants.
- **Organize shared codebase modules:** Place cross-cutting logic in designated root directories under `src/` by locating integrations in `src/lib/`, reusable UI elements in `src/components/`, and shared state abstractions in `src/hooks/`.
