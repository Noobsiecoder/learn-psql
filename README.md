# PostgreSQL

![postgres-image](https://images.g2crowd.com/uploads/product/image/social_landscape/social_landscape_251be2af3ae607c45c14e816eaa1cf41/postgresql.png)

- PostgreSQL is a powerful, open source object-relational database system.
- It has more than 30 years of active development phase and a proven architecture that has earned it a strong reputation for reliability, data integrity, and correctness.

## 🔍 Difference b/w PostgreSQL and SQL?

- SQL and PostgreSQL both have a similar syntax.
- PostgreSQL have certain extra functionalities that aren't in SQL which are as follows :-
- Supports advanced types such as :
  1. array
  2. json
  3. hstore
  4. user-defined type.
- It supports IP Address Data type.
- Also supports partial and bitmap indexes.
- Gives wide range of options to setup triggers.

## 🤔 Where is PostgreSQL used?

- A robust database in the _LAPP_ stack. It stands for Linux, Apache, PostgreSQL, and PHP (or Python and Perl). PostgreSQL is primarily used as a robust back-end database that powers many dynamic websites and web applications.
- General purpose transaction database, large corporations and startups use PostgreSQL as primary databases to support their applications and products.
- Geospatial database PostgreSQL with the _PostGIS_ extension supports geospatial databases for geographic information systems (GIS).

## 💽 Run on terminal

- Run the following command to enter into `psql` mode in terminal :

```bash
# On MacOS/ Windows/ Linux
psql -U postgres
```

- After running, it will prompt for `user <postgres-username>`'s password.
- Enter the corresponding to enter into `psql` mode in terminal.
- To list _all databases_ in the current PostgreSQL database inside `psql` mode in terminal :

```postgres
postgres=# \l
```

- To list _all tables_ in the current PostgreSQL database inside `psql` mode in terminal :

```postgres
postgres=# \dt
```

- To select a _table_ in the current PostgreSQL database inside `psql` mode in terminal :

```postgres
postgres=# \c <table_name>
```

- To execute _psql commands_ from a file :

```postgres
postgres=# \i <file_name>
```

- To _quit_ PostgreSQL from `psql` mode in terminal :

```postgres
postgres=# \q
```

## 📑 Table of contents

1. [Datatypes](bin/src/datatypes.md)
2. [Commands](bin/src/commands.md)
3. [Schema](bin/src/schema.md)
4. [Queries](bin/src/queries.md)
5. [Operators](bin/src/operator.md)
6. [Expressions](bin/src/expression.md)
7. [Clauses](bin/src/clauses.md)

## 📦 Miscellaneous

[My TODO](bin/TODO.md)

### 🧾 Source

[PostgreSQL tutorialspoint](https://www.tutorialspoint.com/postgresql/index.htm)
