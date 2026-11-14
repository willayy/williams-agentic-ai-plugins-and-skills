# General Programming

Instructions for writing computer programs across all languages, covering architecture, design principles, naming conventions, code structure, control flow, and agent development. Use these instructions when designing, implementing, refactoring, or reviewing computer programs.

- **Enforce Separation of Concerns (SoC):** Ensure a piece of code only ever does one thing.
- **Follow Single Responsibility Principle (SRP):** Restrict reasons for code to change to a single actor, person, role, or stakeholder group.
- **Distinguish SoC from SRP:** Use separation of concerns to dictate what code does and single responsibility to govern why code changes.
- **Maintain high cohesion and low coupling:** Design components by grouping related behavior that changes together while minimizing dependencies and state exposure across components.
- **Enforce architectural principles across all scopes:** Apply core design principles including separation of concerns, single responsibility, encapsulation, cohesion, and coupling uniformly across functions, classes, files, and packages.
- **Adhere to the Unix principle:** Write components that do one thing well and compose together through simple, standard interfaces.
- **Use encapsulation:** Present a comprehensive interface for clients while hiding implementation complexity.
- **Prefer composition over redeclaration:** Build complex components through composition of simple, focused, and reusable parts rather than redeclaring behavior.
- **Apply inheritance for shared behavior:** Inherit from a shared parent class when state or behavior is widely shared across entities instead of redeclaring the same fields.
  - Anti-pattern:

    ```py
    # Anti-pattern: adding a position field to all entity classes with an interface
    # instead of having them inherit a shared parent class
    class Positionable(Protocol):
        position: Position

    class Player:
        def __init__(self, position: Position) -> None:
            self.position = position

    class Enemy:
        def __init__(self, position: Position) -> None:
            self.position = position
    ```

  - Correct inheritance:

    ```py
    # Correct: share widely used state through Entity parent
    class Entity:
        def __init__(self, position: Position) -> None:
            self.position = position

    class Player(Entity):
        pass

    class Enemy(Entity):
        pass
    ```

- **Adhere to Law of Demeter (LOD):** Restrict component interactions strictly to immediate dependencies.
  - Violation: `city = order.get_customer().get_address().get_city()`
- **Adhere to Interface Segregation Principle (ISP):** Avoid forcing clients to depend on interfaces or methods they do not use.
- **Adhere to Dependency Inversion Principle (DIP):** Depend on abstractions rather than low-level modules across all architecture tiers.
- **Avoid utils folders or files:** Place code in logical application domains instead of creating generic utils folders or files.
- **Follow verb-preposition-noun function naming:** Name functions using a verb-(optional) preposition-noun structure, adding prepositions whenever applicable.
- **Avoid single-letter variable names:** Disallow single-letter variable names throughout codebases.
- **Avoid abbreviations:** Spell out words completely in variable names without abbreviations.
- **Follow language-specific case styles:** Format variable names according to the casing conventions of the target programming language.
- **Avoid types in names:** Omit data types and type descriptors from variable and parameter names.
- **Avoid Base or Abstract in names:** Omit "Base" or "Abstract" from class names because semantic status should be evident from the class or type definition.
- **Use types instead of units:** Represent units of measurement using dedicated custom types rather than primitive types.
  - Anti-pattern: `delay: int`
  - Correct: `delay: Seconds`
- **Avoid nested calls:** Store return values in intermediate variables before passing them into other functions instead of nesting calls.
  - Violation: `result = process_user(fetch_account(get_user_id()))`
- **Limit indenting and nesting depth:** Restrict nesting depth to at most one level from the root level of a function, file, or class, with an exception only for switch statements.
  - Violation:

    ```py
    for i in range(a):
        for j in range(b):
            # Already illegal
            for k in range(c):
                # Very illegal...
                ...
    ```

- **Enforce line limits:** Limit code lines to no more than 100 characters.
- **Avoid storing data in code:** Externalize credentials, mock data, configuration, and lookup constants rather than storing data in code.
- **Limit anonymous functions:** Restrict anonymous functions to short maps or predicates that do not exceed the line limit.
  - Violation: `users = map(lambda user: format_profile(user.id, user.attributes) if user.is_active else default_profile(user.id), dataset)`
- **Do not generate comments and documentation:** Avoid generating comments and documentation unless explicitly requested.
- **Select appropriate script type for non-reusable tasks:** Use shell scripts for simple system tasks and inline Python executed in the terminal for advanced non-reusable tasks.
- **Store single-use programs in scratch directory:** Place any temporary single-use helper programs solely within the scratch directory.
- **Request permission before running code:** Prompt for explicit user permission before executing any code being worked on.
- **Do not use default arguments:** Avoid defining default parameter values in function signatures.
- **Avoid default returns:** Handle every conditional branch with explicit return values rather than relying on default returns.
- **Reuse open source and standard library:** Use existing functionality from standard libraries or open-source packages instead of reimplementing solutions.
- **Use linting and formatting tools:** Apply available linting and formatting tools to format and validate code whenever they are present in the workspace.
- **Write inline regression tests:** Execute small inline regression tests in the terminal when refactoring to verify that behavior remains invariant.
