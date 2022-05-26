# _ **SELECT queries 101** _

Select query for a specific columns

**SELECT column, another\_column, …**

**FROM mytable;**

Select query for all columns

**SELECT \***

**FROM mytable;**

# _ **Queries with constraints** _

Select query with constraints

**SELECT column, another\_column, …**

**FROM mytable**

**WHERE** _ **condition** _

**AND/OR** _ **another\_condition** _

**AND/OR …;**

| **Operator** | **Condition** |
| --- | --- |
|=, !=, < <=, >, >= | Standard numerical operators |
| BETWEEN … AND … | Number is within range of two values (inclusive) |
| NOT BETWEEN … AND … | Number is not within range of two values (inclusive) |
| IN (…) | Number exists in a list |
| NOT IN (…) | Number does not exist in a list |

# _ **Queries with constraints** _

| **Operator** | **Condition** |
| --- | --- |
| = | Case sensitive exact string comparison ( **notice the single equals** ) |
| != or <> | Case sensitive exact string inequality comparison |
| LIKE | Case insensitive exact string comparison |
| NOT LIKE | Case insensitive exact string inequality comparison |
| % | Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE) |
| \_ | Used anywhere in a string to match a single character (only with LIKE or NOT LIKE) |
| IN (…) | String exists in a list |
| NOT IN (…) | String does not exist in a list |

# _ **Filtering and sorting Query results** _

**SELECT**** DISTINCT **** column**

**DISTINCT**  keyword will blindly remove duplicate rows

**ORDER**** BY **** column **** ASC ****/**** DESC**

**LIMIT**  **num\_limit**  **OFFSET**  **num\_offset;**

**ORDER BY**  clause will alpha-numerically sort each row based on the specified column&#39;s value.

**LIMIT**  will reduce the number of rows to return

**OFFSET**  will specify where to begin counting the number rows from

**ASC**** / ****DESC** is the keyword used to sort result sets in either ascending or descending order.

# _ **Multi-table queries with JOINs** _

**FROM mytable**

**INNER JOIN another\_table**

**ON mytable.id = another\_table.id**

The  **INNER JOIN**  is a process that matches rows from the first table and the second table which have the same key (as defined by the  **ON**  constraint) to create a result row with the combined columns from both tables. After the tables are joined

# _ **Inserting rows** _

**INSERT INTO mytable**

**(column, another\_column, …)**  **=> without this line means all columns**

**VALUES (value\_or\_expr, another\_value\_or\_expr, …),**

**(value\_or\_expr\_2, another\_value\_or\_expr\_2, …),**

… **;**

the number of values need to match the number of columns

# _ **Updating rows** _

**UPDATE mytable**

**SET column = value\_or\_expr,**

**other\_column = another\_value\_or\_expr,**

…

**WHERE condition;**

# _ **Deleting rows** _

**DELETE FROM mytable**

**WHERE condition;**

# _ **Creating tables** _

**CREATE TABLE IF NOT EXISTS mytable (**

**column** _ **DataType** __ **TableConstraint** _ **DEFAULT** _ **default\_value** _ **,**

**another\_column** _ **DataType** __ **TableConstraint** _ **DEFAULT** _ **default\_value** _ **,**

…

**);**

| **Data type** |
| --- |
| **INTEGER** , **=> **integer values**   **BOOLEAN **=> integer value of just 0 or 1** |
| **FLOAT** ,  **DOUBLE** ,  **REAL **=> precise numerical data** |
| **CHARACTER(max num\_chars)**, **VARCHAR(max num\_chars)**,  **TEXT **=> strings and text** |
| **DATE** ,  **DATETIME **=> date and time stamps** |
| **BLOB **=> binary data in blobs** |
| **Description** |

| **Constraint** |
| --- |
| **PRIMARY KEY **=>** unique values(identify a single row) |
| **AUTOINCREMENT **=>** automatically filled integer value in and incremented with each row insertion |
| **UNIQUE **=>** values in this column have to be unique, so you can&#39;t insert another row with the same value in this column as another row in the table |
| **NOT NULL **=>** cannot be `NULL` |
| **CHECK (expression) **=>** run a more complex expression to test whether the values inserted are valid |
| **FOREIGN KEY **=>** ensures that each value in this column corresponds to another value in a column in another table |

Note that : **UNIQUE** Differs from the PRIMARY KEY in that it doesn&#39;t have to be a key for a row in the table.

# _ **Altering tables** _

**ALTER TABLE**  statement to add, remove, or modify columns and table constraints

Altering table to add new column(s)

ALTERTABLE mytable

**ADD column** _ **DataType** __ **OptionalTableConstraint** _

**DEFAULT default\_value;**

Altering table to remove column(s)

**ALTER TABLE mytable**

**DROP column\_to\_be\_deleted;**

Altering table name

**ALTER TABLE mytable**

**RENAME TO new\_table\_name;**

# _ **Dropping tables** _

Drop table statement

**DROP TABLE IF EXISTS mytable;**


**Here is the solution for sqlbolt site exercises**
[sqlbolt web site](https://sqlbolt.com/)

![img](../sql/screenshots/Screenshot%20(62).png)
![img](../sql/screenshots/Screenshot%20(63).png)
![img](../sql/screenshots/Screenshot%20(64).png)
![img](../sql/screenshots/Screenshot%20(65).png)
![img](../sql/screenshots/Screenshot%20(66).png)
![img](../sql/screenshots/Screenshot%20(67).png)
![img](../sql/screenshots/Screenshot%20(68).png)
![img](../sql/screenshots/Screenshot%20(69).png)
![img](../sql/screenshots/Screenshot%20(70).png)
![img](../sql/screenshots/Screenshot%20(71).png)
![img](../sql/screenshots/Screenshot%20(72).png)
![img](../sql/screenshots/Screenshot%20(73).png)
![img](../sql/screenshots/Screenshot%20(74).png)
![img](../sql/screenshots/Screenshot%20(75).png)
![img](../sql/screenshots/Screenshot%20(76).png)
![img](../sql/screenshots/Screenshot%20(77).png)
![img](../sql/screenshots/Screenshot%20(78).png)
![img](../sql/screenshots/Screenshot%20(79).png)
![img](../sql/screenshots/Screenshot%20(80).png)
![img](../sql/screenshots/Screenshot%20(81).png)
![img](../sql/screenshots/Screenshot%20(82).png)
![img](../sql/screenshots/Screenshot%20(83).png)
![img](../sql/screenshots/Screenshot%20(84).png)
![img](../sql/screenshots/Screenshot%20(85).png)
![img](../sql/screenshots/Screenshot%20(86).png)
![img](../sql/screenshots/Screenshot%20(87).png)
![img](../sql/screenshots/Screenshot%20(88).png)
![img](../sql/screenshots/Screenshot%20(89).png)
![img](../sql/screenshots/Screenshot%20(90).png)
![img](../sql/screenshots/Screenshot%20(91).png)
![img](../sql/screenshots/Screenshot%20(92).png)
![img](../sql/screenshots/Screenshot%20(93).png)
![img](../sql/screenshots/Screenshot%20(94).png)
![img](../sql/screenshots/Screenshot%20(95).png)
![img](../sql/screenshots/Screenshot%20(96).png)
![img](../sql/screenshots/Screenshot%20(97).png)
![img](../sql/screenshots/Screenshot%20(98).png)
![img](../sql/screenshots/Screenshot%20(99).png)
![img](../sql/screenshots/Screenshot%20(100).png)
![img](../sql/screenshots/Screenshot%20(101).png)








