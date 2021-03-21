# Introduction

- PostgreSQL supports a wide set of Data Types.
- Besides, users can create their own custom data type using `CREATE TYPE { SQL }` command.
- There are different categories of data types in PostgreSQL.

### Numeric Data Type

![num_image](../img/numeric_data_type.png)

### Monetary Data Type

![monetary_image](../img/monetary_data_type.png)

### Character Data Type

![char_image](../img/char_data_type.png)

### Binary Data Type

![bin_image](../img/bin_data_type.png)

### Date/Time Data Type

![date/time_image](../img/date_time_data_type.png)

### Boolean Data Type

![bool_image](../img/bool_data_type.png)

### Enumerated Data Type

- Enumerated (enum) types are data types that comprise a static, ordered set of values.
- They are equivalent to the enum types supported in a number of programming languages.
- For instance :

```postgresql
CREATE TYPE days AS ENUM("Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun" );
```

### Geometric Data Type

- They represent two dimensional spatial objects :
  ![geo_image](../img/geo_data_type.png)

### Network Data Type

- They represent two dimensional spatial objects :
  ![net_image](../img/net_data_type.png)

### JSON Data Type

![json_image](../img/json_data_type.png)
