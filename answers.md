State and Explain the components of a DBMS(Database Management System)
1. Database Engine
The database engine is the core of a DBMS. It handles the actual storing, retrieving, and updating of data. When you run a query like SELECT * FROM users, the engine processes it and fetches the results. It also ensures that all transactions are completed properly and maintains the consistency and integrity of the data.

2. Data Definition Component
This component is responsible for defining the structure of the database. It works with the Data Definition Language (DDL), which includes commands like CREATE TABLE and ALTER TABLE. You use this to define tables, relationships, and constraints like primary keys or foreign keys.

3. Data Manipulation Component
This handles operations that modify or retrieve data, using the Data Manipulation Language (DML). Commands like INSERT, UPDATE, DELETE, and SELECT are all part of this. It’s the part of the DBMS you interact with when working directly with the data.

4. Data Storage Management
This component is in charge of how data is stored on physical storage like hard drives or SSDs. It optimizes data storage for fast access and retrieval, often using techniques like indexing to speed up queries.

5. Metadata Management
Metadata is “data about data,” and this component stores it. For example, it keeps track of table structures, column types, relationships, and user permissions. If you use a command like DESCRIBE table_name, the DBMS fetches this information from the metadata.

6. Query Processor
The query processor takes your SQL commands, checks their syntax, and figures out how to execute them in the most efficient way. It’s made up of a parser (to understand the query) and an optimizer (to improve performance).

7. Transaction Management
This component ensures that transactions are handled reliably by following the ACID properties (Atomicity, Consistency, Isolation, Durability). For example, in a banking app, it ensures that money is either transferred completely or not at all if an error occurs.

8. Security Management
The security management component controls access to the database. It makes sure only authorized users can view or modify the data. It includes features like user authentication, roles, permissions, and sometimes encryption for sensitive data.

9. Backup and Recovery
This component ensures that your data is safe by creating backups. It also helps restore the database in case of crashes or data corruption, minimizing the risk of data loss.

10. User Interface
The user interface is how users interact with the DBMS. It can be a command-line tool, a graphical interface like phpMyAdmin, or even APIs that applications use to connect to the database.



 What is a relational database? Give 4 examples.


A relational database is a type of database that stores and organizes data in tables, which are made up of rows and columns. Each table, also known as a relation, represents a specific entity (e.g., customers, products) and has a unique structure defined by its columns (attributes). Rows in the table, also called records or tuples, represent individual data entries.
The key characteristic of a relational database is its ability to establish relationships between tables using keys. For example, a primary key in one table can act as a foreign key in another, creating a link between related data. Structured Query Language (SQL) is commonly used to interact with and manage relational databases.

Examples of Relational Databases:
1. MySQL
MySQL is an open-source relational database management system widely used for web applications and services, such as WordPress websites.

2. PostgreSQL
PostgreSQL is a powerful, open-source relational database known for its advanced features, such as support for custom functions and scalability.

3. Oracle Database
Oracle is a commercial relational database system designed for large-scale enterprise applications with high-performance requirements.

4. Microsoft SQL Server
SQL Server is a relational database management system developed by Microsoft, commonly used in enterprise environments for data analysis and reporting.



State and Explain three classifications of SQL?

SQL (Structured Query Language) is classified into different categories based on the types of operations it performs on a database. Here are three main classifications of SQL:

1. Data Definition Language (DDL)
DDL deals with defining and modifying the structure of the database, such as creating, altering, or deleting database objects like tables, indexes, and schemas. These commands are executed automatically (without needing a COMMIT statement) and directly affect the database structure.
Examples of DDL Commands:
CREATE: Used to create new database objects, like CREATE TABLE students (...);.
ALTER: Modifies existing objects, like adding a column to a table using ALTER TABLE students ADD age INT;.
DROP: Deletes objects, like removing a table with DROP TABLE students;.
TRUNCATE: Deletes all data from a table but keeps its structure.

2. Data Manipulation Language (DML)
DML focuses on managing the data within the database. It allows users to insert, retrieve, update, or delete data. Unlike DDL, DML operations require explicit saving of changes using a COMMIT statement (or they can be rolled back using ROLLBACK).
Examples of DML Commands:
INSERT: Adds new records to a table, like INSERT INTO students (name, age) VALUES ('Alice', 20);.
SELECT: Retrieves data, like SELECT * FROM students;.
UPDATE: Modifies existing records, like UPDATE students SET age = 21 WHERE name = 'Alice';.
DELETE: Removes specific records, like DELETE FROM students WHERE age < 18;.

3. Data Control Language (DCL)
DCL manages access control and permissions within the database. It allows database administrators to grant or revoke privileges to users or roles, ensuring the security and integrity of the data.
Examples of DCL Commands:
GRANT: Assigns privileges, like GRANT SELECT ON students TO user1;.
REVOKE: Removes previously granted permissions, like REVOKE SELECT ON students FROM user1;.



What is the difference between a Primary Key and a Foreign Key?

A Primary Key is a unique identifier for a record in a table, ensuring each record is distinct. It cannot have null values and guarantees uniqueness. For example, a student_id in a students table.
A Foreign Key is a column in one table that references the primary key of another table, creating a relationship between them. It can have duplicates and null values. For example, student_id in an enrollments table that refers to student_id in the students table.
Key Differences:
Primary Key: Unique, no nulls, defines record identity in the same table.
Foreign Key: References a primary key from another table, can have duplicates or nulls.



What is an Entity-Relationship Diagram?


An Entity-Relationship (ER) Diagram is a visual representation of the entities (objects or concepts) in a system and the relationships between them. It is commonly used in database design to illustrate how data is structured and how different pieces of data relate to each other.



What are the advantages of relational databases?


Data Integrity: Enforces rules like primary keys and constraints, ensuring data consistency and accuracy.
Structured Organization: Data is stored in organized tables, making it easy to manage relationships and retrieve data with SQL.
Scalability: Can handle large datasets and grow as needed.
Security: Provides features like user authentication and access control.
ACID Compliance: Ensures reliable transactions with properties like Atomicity and Durability.
Data Independence: Allows changes to the database structure without affecting applications.
Efficient Querying: Supports complex queries for quick data retrieval.
Standardization: Uses SQL, making it easy to work with different database systems.



State four types of data type used to store data in tables?

INTEGER: Used to store whole numbers without decimals. For example, age or quantity.
VARCHAR: Used to store variable-length strings, such as names, addresses, or descriptions.
DATE: Used to store date values (year, month, day), often used for birthdates, transaction dates, etc.
DECIMAL: Used to store numbers with fixed decimal points, ideal for monetary values or measurements where precision is important.



What is the purpose of a database management system (DBMS)? 


Data Storage: Organizes data in tables for easy management.
Data Retrieval: Allows querying and updating data.
Security: Ensures data privacy through access control.
Data Integrity: Maintains accurate and consistent data.
Concurrency Control: Supports multiple users accessing data simultaneously.
Backup and Recovery: Protects data with backup and recovery features.

