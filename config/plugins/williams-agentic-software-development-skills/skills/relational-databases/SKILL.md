---
name: relational-databases
description: Instructions for designing, altering, and validating relational databases; use when defining database schemas, creating constraints, or normalizing tables.
---

# Relational Databases

Instructions for designing, altering, and validating relational databases. Use this skill when defining database schemas, creating constraints, or normalizing tables.

- **Model distinct entities:** Group attributes by the real-world concept they belong to, ensuring attributes in the same table describe the same core entity, share the primary key, and lifecycle together.
- **Map relationship cardinality:** Isolate relationships systematically by keeping 1:1 entities in the same table, placing foreign keys on the many side for 1:N relations, and creating junction tables for N:M relations.
- **Enforce normalization standards:** Ensure every normalized table satisfies 3NF where every non-key attribute holds a single atomic value and depends strictly on the entire primary key alone.
- **Standardize constraint identifiers:** Format constraint names systematically using prefixes `pk_<table>`, `fk_<source>_<target>`, `uq_<table>_<column>`, `chk_<table>_<purpose>`, and `df_<table>_<column>`.
- **Define nullability and cascades:** Default columns to NOT NULL unless missing values convey explicit domain semantics, and specify foreign key deletion behaviors explicitly rather than relying on engine defaults.
- **Restrict check constraint scope:** Confine CHECK constraints strictly to columns within the evaluated row, never referencing external tables, subqueries, or volatile functions.
- **Prioritize declarative constraints:** Enforce data validation rules through declarative constraints first, resorting to database triggers only when constraints cannot model the invariant.
- **Isolate business logic:** Limit the database engine strictly to relational integrity and CRUD operations, encapsulating all business workflow logic within the application tier.
