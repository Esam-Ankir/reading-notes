# SQL vs. NoSQL

***SQL database examples:*** 

MySql, Oracle, Sqlite, Postgres and MS-SQL. 


***NoSQL database examples:*** 

MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb

## Common types of NoSQL
### Key-value stores
- Array of key-value pairs. The "key" is an attribute name.
- Redis, Vodemort, Dynamo.

### Document databases
- Data is stored in documents.
- Documents are grouped in collections.
- Each document can have an entirely different structure.
- CouchDB, MongoDB.

### Wide-column / columnar databases
- Column families - containers for rows.
- No need to know all the columns up front.
- Each row can have different number of columns.
- Cassandra, HBase.

### Graph database
- Data is stored in graph structures
  - Nodes: entities
  - Properties: information about the entities
  - Lines: connections between the entities
- Neo4J, InfiniteGraph

## Differences between SQL and NoSQL
### Storage
- SQL: store data in tables.
- NoSQL: have different data storage models.

### Schema
- SQL
  - Each record conforms to a fixed schema.
  - Schema can be altered, but it requires modifying the whole database.
- NoSQL:
  - Schemas are dynamic.

### Querying
- SQL
  - Use SQL (structured query language) for defining and manipulating the data.
- NoSQL
  - Queries are focused on a collection of documents.
  - UnQL (unstructured query language).
  - Different databases have different syntax.

### Scalability
- SQL
  - Vertically scalable (by increasing the horsepower: memory, CPU, etc) and expensive.
  - Horizontally scalable (across multiple servers); but it can be challenging and time-consuming.
- NoSQL
  - Horizontablly scalable (by adding more servers) and cheap.

### ACID
- Atomicity, consistency, isolation, durability
- SQL
  - ACID compliant
  - Data reliability
  - Gurantee of transactions
- NoSQL
  - Most sacrifice ACID compliance for performance and scalability.

## Which one to use?
### SQL
- Ensure ACID compliance.
  - Reduce anomalies.
  - Protect database integrity.
- Data is structured and unchanging.

### NoSQL
- Data has little or no structure.
- Make the most of cloud computing and storage.
  - Cloud-based storage requires data to be easily spread across multiple servers to scale up.
- Rapid development.
  - Frequent updates to the data structure.

## Data Modeling

- The Table Name, which is located at the top of the table.

- The Primary Keys.  Remember the primary keys uniquely identify each row in a table.  A table typically has one primary key, but can have more.  When the key has more than one column, it is called a compound key.

- Table Columns – There can be one or more table columns.  To keep the diagrams simple, I don’t show the data types.  I may introduce those later when we focus on more comprehensive modeling.

- Foreign Key – This is a column or set of columns which match a primary key in another table.
	

### Data Modeling – Table Relationships

- zero or one-to-many	0..*

- one-to-many	1..*

- zero or one-to-one	0..1

- one-to-one	1..1

## Sequelize v6

Sequelize is a promise-based Node.js ORM tool for Postgres, MySQL, MariaDB, SQLite, Microsoft SQL Server, Amazon Redshift and Snowflake’s Data Cloud. It features solid transaction support, relations, eager and lazy loading, read replication and more.

Sequelize follows Semantic Versioning and supports Node v10 and above.

	

