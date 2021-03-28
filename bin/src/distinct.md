# Introduction

- The PostgreSQL `DISTINCT` keyword is used in conjunction with `SELECT` statement to eliminate all the duplicate records and fetching only unique records.

## Syntax

```postgresql
SELECT DISTINCT col[1], col[2]
FROM <table_name>
WHERE [condition];
```

## Example

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

- Let's add some data that already exists with different values except for the _name_ column.

  ```postgres
  INSERT INTO users VALUES (2, 'Allen', '25', 'Texas', '15000');
  INSERT INTO users VALUES (4, 'Mark', '25', 'Rich-Mond', '65000');
  ```

- Now the table looks like :

  | id  | name  | age | address    | salary |
  | --- | ----- | --- | ---------- | ------ |
  | 1   | Paul  | 32  | California | 20000  |
  | 2   | Allen | 25  | Texas      | 15000  |
  | 3   | Teddy | 23  | Norway     | 20000  |
  | 4   | Mark  | 25  | Rich-Mond  | 65000  |
  | 5   | David | 27  | Texas      | 85000  |
  | 6   | Kim   | 22  | South-Hall | 45000  |
  | 7   | James | 24  | Houston    | 10000  |
  | 2   | Allen | 25  | Texas      | 15000  |
  | 4   | Mark  | 25  | Rich-Mond  | 65000  |

- Now run the following commands :

  ```postgres
  SELECT * FROM users;
  ```

- We'll get :

  ```postgres
  id | name  | age |  address   | salary
  ----+-------+-----+------------+--------
    1 | Paul  | 32  | California | 20000
    2 | Allen | 25  | Texas      | 15000
    3 | Teddy | 23  | Norway     | 20000
    4 | Mark  | 25  | Rich-Mond  | 65000
    5 | David | 27  | Texas      | 85000
    6 | Kim   | 22  | South-Hall | 45000
    7 | James | 24  | Houston    | 10000
    2 | Allen | 25  | Texas      | 15000
    4 | Mark  | 25  | Rich-Mond  | 65000
  (9 rows)
  ```

- Some of the rows are duplicated. To get only distinct rows :

  ```postgres
  SELECT DISTINCT * FROM users;
  ```

- Hence the result will be :

  ```postgres
  id | name  | age |  address   | salary
  ----+-------+-----+------------+--------
    1 | Paul  | 32  | California | 20000
    2 | Allen | 25  | Texas      | 15000
    4 | Mark  | 25  | Rich-Mond  | 65000
    3 | Teddy | 23  | Norway     | 20000
    5 | David | 27  | Texas      | 85000
    6 | Kim   | 22  | South-Hall | 45000
    7 | James | 24  | Houston    | 10000
  ```
