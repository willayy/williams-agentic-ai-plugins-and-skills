# General Programming Instructions

Computer Language agnostic rules that should be followed when writing any computer program.

## Architecture & Design Principles

- **Enforce Separation of Concerns (SoC):** A piece of code should ever only do one thing.
- **Follow Single Responsibility Principle (SRP):** A piece of code should only have one reason to change, where a "reason to change" refers to an actor—a single person, role, or stakeholder group that requests changes to the software.
- **Distinguish SoC from SRP:** Separation of concerns dictates what the code does (ensuring a piece of code only does one thing), whereas SRP dictates why the code changes (ensuring a piece of code only changes for a single actor).
- **Maintain high cohesion and low coupling:** Design components with high cohesion by grouping related behavior and data that change together, and maintain low coupling by minimizing dependencies and state exposure between components.
- **Enforce architectural principles across all scopes:** Apply core design principles—such as SoC, SRP, encapsulation, cohesion, and coupling—uniformly across functions, classes, files, and packages.
- **Adhere to the Unix principle:** Write programs and components that do one thing and do it well, and compose together through simple, standard interfaces.
- **Use encapsulation:** Encapsulation should always be used to present a comprehensive interface for clients and hide complexity.
- **Prefer composition over redeclaration:** Build complex objects and components through composition of simple, focused and reusable parts rather than redeclaring behavior.
- **Apply inheritance for shared behavior:** Generally build objects through composition of simpler objects, but if behavior is widely shared then inheritance SHOULD be used instead of adding the same object field to all classes.
- **Adhere to Law of Demeter (LOD):** Adhere to the Law of Demeter (the principle of least knowledge, stating that an object or component should only interact with its immediate dependencies).
- **Adhere to Interface Segregation Principle (ISP):** Adhere to the Interface Segregation Principle, clients should not be forced to depend on interfaces or methods they do not use.
- **Adhere to Dependency Inversion Principle (DIP):** Adhere to the Dependency Inversion Principle, high-level modules should not depend on low-level modules; both should depend on abstractions.
- **Avoid utils folders or files:** Do not create utils folders or files; if you cannot find a logical place for code in your application, consider whether it is actually needed.

**Examples of Law of Demeter (LOD) violations:**
```py
city = order.get_customer().get_address().get_city()
```

**Examples of composition anti-patterns:**
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

# Correct: share widely used state through Entity parent
class Entity:
    def __init__(self, position: Position) -> None:
        self.position = position

class Player(Entity):
    pass

class Enemy(Entity):
    pass
```

## Naming Conventions

- **Follow verb-preposition-noun function naming:** Functions should always follow a verb-(optional) preposition-noun structure (e.g. send_emails); if a preposition can be added, it should be added (e.g. transform_to_json).
- **Avoid single-letter variable names:** Do not use single-letter variable names.
- **Avoid abbreviations:** Do not use abbreviations in variable names and spell out words completely.
- **Follow language-specific case styles:** Format variable names according to the casing conventions of the target programming language.
- **Avoid types in names:** Do not include data types or type descriptors in variable names.
- **Avoid Base or Abstract in names:** Do not use "Base" or "Abstract" in names because this should be semantically clear from the type or class itself.
- **Use types instead of units:** Use dedicated types instead of primitive types to represent units of measurement.

**Examples of using types instead of units:**
```py
# Anti-pattern: using a primitive type for a unit
delay: int

# Correct: using a dedicated type for a unit
delay: Seconds
```

## Code Structure & Control Flow

- **Avoid nested calls:** Function calls should not be nested; call a function, store the return value in a variable, and then pass the variable.
- **Limit indenting and nesting depth:** No code, except switch statements, may nest deeper than one level from the root level of a function, file or class.
- **Enforce line limits:** Lines of code should not span more than 100 characters.
- **Avoid storing data in code:** Do not store data—including credentials, mock data, configs, and lookup constants—in code.
- **Limit anonymous functions:** Anonymous functions should never bypass the line limit, though shorter ones used for maps and predicates are acceptable.

**Examples of illegal nesting:**
```py
for i in range(a):
    for j in range (b):
        # Already illegal
        for k in range(c):
            # Very illegal...
            ...
```

**Examples of illegal nested calls:**
```py
result = process_user(fetch_account(get_user_id()))
```

**Examples of illegal anonymous functions:**
```py
users = map(lambda user: format_profile(user.id, user.attributes) if user.is_active else default_profile(user.id), dataset)
```

# Agent Development Instructions

Rules for managing agents in agentic software engineering.

- **Do not generate comments and documentation:** Do not generate comments and documentation unless explicitly asked to.
- **Select appropriate script type for non-reusable tasks:** Prefer shell scripts for simple tasks and general systems tasks. Use inline Python code through the terminal for more advanced tasks.
- **Store single-use programs in scratch directory:** Any extra programs written by the agent to complete a task should be placed in the scratch directory nowhere else.
- **Request permission before running code:** Always ask if code being worked on should be run or not.
- **Do not use default arguments:** Agents should never use default arguments.
- **Avoid default returns:** Functions should avoid default returns and explicitly handle every return path.
- **Reuse open source and standard library:** Never implement software or functionality that can be obtained from an open source package or the standard library.

# Git Instructions

Rules for how to create git commits, based on the conventional commits specification.

- **Follow commit message format:** `<type>(scope): <description>` followed by an optional body.
- **Target individual software objects:** A software object is defined as a function, method, class, global constant, global variable, configuration file, or documentation file.
- **Identify broken behavior for fixes:** Any segment of code that is producing unintended, unexpected (that is, it is not a documented and accepted unintended behavior) behavior.
- **Apply standard commit prefixes:** `feat` (used when a new SO is added/written), `fix` (used when any change on an existing SO has the purpose of fixing something that is broken), `refactor` (used when any change on an existing SO does NOT have the purpose of fixing something that is broken, including moving, relocating, or refactoring existing code without changing external behavior), `docs` (used when a documentation SO is added or modified), `test` (used when adding or modifying test SOs), `chore` (used for configuration file SOs, build scripts, or dependency maintenance), and `perf` (used for a code change on an existing SO that improves performance).
- **Format description with allowed imperative verbs:** The `<description>` must be written in lowercase imperative mood and must start with one of the allowed verbs: `add`, `allow`, `enforce`, `extract`, `move`, `prevent`, `remove`, `rename`, `swap`, or `update`.
- **Limit commits to a single software object change:** Exactly one commit per individual SO change. Never group changes to multiple SOs into a single commit.

**Examples of commit messages:**
```txt
feat(auth): add verify_token method
fix(parser): prevent null reference when input is empty
refactor(models): move user_validator to separate module
refactor(auth): rename user_token to auth_token
refactor(cache): swap redis_client with memcached_client
docs(readme): add installation instructions
```
