# Introduction

- A schema is a named collection of tables.
- It can contain :
  1. Views
  2. Indexes
  3. Sequences
  4. Data types
  5. Operators
  6. Functions
- Schemas are analogous to directories at the operating system level, except that schemas cannot be nested.

## Advantages of using a Schema

- It allows many users to use one database without interfering with each other.
- It organizes database objects into logical groups to make them more manageable.
- Third-party applications can be put into separate schemas so they do not collide with the names of other objects.

## Commands

1. Create _Schema_ :

```postgresql
CREATE SCHEMA IF NOT EXISTS <schema_name>;
```

2. Create _Table in Schema_ :

```postgresql
CREATE TABLE IF NOT EXISTS <schema_name>.<table_name (
  NAME VARCHAR (20) NOT NULL,
  AGE  INT          NOT NULL
);
```

3. Drop _Schema_ :

```postgresql
DROP SCHEMA IF NOT EXISTS <schema_name>;
```

### Source

[PostgreSQL tutorialspoint](https://www.tutorialspoint.com/postgresql/postgresql_schema.htm)
