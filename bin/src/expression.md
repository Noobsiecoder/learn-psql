# Introduction

- An expression is a combination of one or more values, operators, and PostgresSQL functions that evaluate to a value.
- PostgreSQL expressions are like formulas and they are written in query language.
- You can also use to query the database for specific set of data.

## Syntax

```postgresql
SELECT col[1], col[2], col[3]
FROM <table_name>
WHERE [condition | expression];
```

## Built-in methods

- There are several built-in functions like `avg()`, `sum()`, `count()`
- This is to perform what is known as _aggregate data calculations_ against a table or a specific table column.
- Consider a **table** in _PostgreSQL database_ :

  | id  | name  | age | address    | salary |
  | --- | ----- | --- | ---------- | ------ |
  | 1   | Paul  | 32  | California | 20000  |
  | 2   | Allen | 25  | Texas      | 15000  |
  | 3   | Teddy | 23  | Norway     | 20000  |
  | 4   | Mark  | 25  | Rich-Mond  | 65000  |
  | 5   | David | 27  | Texas      | 85000  |
  | 6   | Kim   | 22  | South-Hall | 45000  |
  | 7   | James | 24  | Houston    | 10000  |

- If we run the following command :

  ```postgresql
  SELECT COUNT(*) AS "RECORDS" FROM COMPANY;
  ```

- The result will be :

  ```postgresql
  RECORDS
  ---------
        7
  (1 row)
  ```
