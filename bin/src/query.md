# Introduction

- A query is a way of requesting information from the database.
- A database query can be either a _select query_ or an _action query_.
- _Select query_ is a query for retrieving data
- _Action query_ requests additional actions to be performed on the data, like deletion, insertion, and updating.

## Select Query

### INSERT command

- The PostgreSQL `INSERT INTO` statement allows one to insert new rows into a table.
- One can insert a single row at a time or several rows as a result of a query.
- Syntax :

  ```postgresql
  INSERT INTO <table_name> (col[1], col[2], ...col[N]) VALUES (val[1], val[2],...val[N]);
  ```

- if we add for all columns, we needn't specify the column :

  ```postgresql
  INSERT INTO <table_name> VALUES (val[1], val[2],...val[N]);
  ```

### SELECT command

- PostgreSQL `SELECT` statement is used to fetch the data from a database table, which returns data in the form of result table.
- These result tables are called **result-sets**.
- Syntax :

  ```postgresql
  SELECT col[1], col[2], col[N] FROM <table_name>;
  ```

- For selecting all columns from the table :

  ```postgresql
  SELECT * FROM <table_name>;
  ```

### UPDATE command

- The PostgreSQL `UPDATE` Query is used to modify the existing records in a table.
- You can use `WHERE` clause with `UPDATE` query to update the selected rows.
- Otherwise, all the rows would be updated.
- Syntax :

  ```postgresql
  UPDATE <table_name>
  SET col[1] = <rand_val>
  WHERE [condition];
  ```

### DELETE command

- The PostgreSQL `DELETE` Query is used to delete the existing records from a table.
- You can use `WHERE` clause with` DELETE` query to delete the selected rows.
- Otherwise, all the records would be deleted.
- Syntax :

  ```postgresql
  DELETE FROM <table_name>
  WHERE [condition];
  ```
