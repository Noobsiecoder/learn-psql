# Introduction

- Constraints are the rules enforced on data columns on table.
- These are used to prevent invalid data from being entered into the database.
- This ensures the accuracy and reliability of the data in the database.

## Types of constraints

| Constraints   | How they work                                                  |
| ------------- | -------------------------------------------------------------- |
| `NOT NULL`    | Ensures that a column cannot have `NULL` value                 |
| `UNIQUE`      | Ensures that all values in a column are different              |
| `PRIMARY KEY` | Uniquely identifies each row/record in a database table        |
| `FOREIGN KEY` | Constrains data based on columns in other tables               |
| `CHECK`       | Ensures that all values in a column satisfy certain conditions |

## Examples

1. `NOT NULL`

   ```postgres
   CREATE TABLE IF NOT EXISTS users (
       EMAIL_ID VARCHAR(255) NOT NULL,
       PASS_WORD VARCHAR(255) NOT NULL,
   );
   ```

2. `UNIQUE`

   ```postgres
   CREATE TABLE IF NOT EXISTS users (
       USER_NAME VARCHAR(255) UNIQUE NOT NULL,
       EMAIL_ID VARCHAR(255) NOT NULL,
       PASS_WORD VARCHAR(255) NOT NULL,
   );
   ```

3. `PRIMARY KEY`

   ```postgres
   CREATE TABLE IF NOT EXISTS users (
       UUID SERIAL PRIMARY KEY UNIQUE NOT NULL,
       USER_NAME VARCHAR(255) UNIQUE NOT NULL,
       EMAIL_ID VARCHAR(255) NOT NULL,
       PASS_WORD VARCHAR(255) NOT NULL,
   );
   ```

4. `FOREIGN KEY`

- Create a table named _users_ :

  ```postgres
  CREATE TABLE IF NOT EXISTS users (
       UUID SERIAL PRIMARY KEY UNIQUE NOT NULL,
       USER_NAME VARCHAR(255) UNIQUE NOT NULL,
       EMAIL_ID VARCHAR(255) NOT NULL,
       PASS_WORD VARCHAR(255) NOT NULL,
   );
  ```

- Now create another table named _friends_ which references to `ID` from table _users_ :

  ```postgres
  CREATE TABLE IF NOT EXISTS friends (
      FRIEND_NAME VARCHAR(255) UNIQUE NOT NULL,
      USER_ID SERIAL REFERENCES users(UUID)
  );
  ```

5. `CHECK`

   ```postgres
   CREATE TABLE IF NOT EXISTS employees (
       ID SERIAL PRIMARY KEY,
       NAME VARCHAR(255) UNIQUE NOT NULL,
       AGE VARCHAR(255) NOT NULL,
       ADDRESS VARCHAR(255) NOT NULL,
       SALARY REAL CHECK ( SALARY > 0 )
   );
   ```

## Drop constraints

- To remove a constraint you need to know its name.
- If the name is known, it is easy to drop. 
- Else, you need to find out the system-generated name. 
- The psql command `\d` table name can be helpful here. 
- The general syntax is :

```postgres
ALTER TABLE <table_name> DROP CONSTRAINT <constraint_name>;
```
