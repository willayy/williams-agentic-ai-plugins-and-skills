---
name: relational-database
description: Rules for designing, altering, and validating relational databases.
---

# Relational Database

Rules for designing, altering, and validating relational databases.

- **Model distinct entities:** Group attributes by the real-world concept they belong to; attributes belong in the same table if they describe the same core entity, share the same primary key, and are created and modified together.
- **Map cardinality to keys:** Separate data into different tables based on entity relationships: keep One-to-One (1:1) in the same table by default, put foreign keys on the "many" side for One-to-Many (1:N), and use an intermediate junction table for Many-to-Many (N:M).
- **Apply 3NF dependency rule:** In a normalized table, every column must hold a single atomic value, depend directly on the entire primary key, and not depend on another non-key column.
- **Constraint naming convention:** Format constraint names systematically using `pk_<table>` (Primary Key), `fk_<source_table>_<target_table>` (Foreign Key), `uq_<table>_<column>` (Unique), `chk_<table>_<purpose>` (Check), and `df_<table>_<column>` (Default).
- **Nullability and delete behavior:** Default columns to NOT NULL unless an empty value has an intentional meaning, and always explicitly define foreign key deletion behavior rather than relying on engine defaults.
- **Keep CHECK constraints independent:** A CHECK constraint must only evaluate data inside the current row and never reference other tables or volatile values.
- **Constraints versus triggers:** Always use a constraint by default; use a trigger only when a constraint cannot express the rule.
- **CRUD only:** The database should only serve CRUD operations; all business logic must remain application-side.
