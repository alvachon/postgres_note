# PostgreSQL Notes

## Introduction
PostgreSQL is the most popular open source relational database
 
 # #  Installation
### Install on Ubuntu
```
sudo apt update
sudo apt upgrade
sudo apt install postgresql postgresql-contrib
sudo apt-get install postgresql-(version)
```

### Install pgAdmin 4 on Ubuntu (GUI)
[Official Page](https://www.pgadmin.org/download/pgadmin-4-apt/)

### General information
```
man psql
psql --help 
``` 

### Calling the program
```
sudo -i -u postgres
psql
```
### View command
List of databases
```
\l
```

List of roles
```
\du
```

### Modify or Create  or Delete role
```
ALTER USER (role) WITH PASSWORD '(password)';
CREATE USER (new role) WITH PASSWORD '(password)';
ALTER USER (role) WITH SUPERUSER;
DROP USER (role);
```

### How to link pgAdmin 4 with postgres
*Open pgAdmin4, open a new server registration.* \
**Name :** Localhost \
**Host :** 127.0.0.1 (Local Host) \
**Username :** (role with superuser in postgres) \
**Password :** (the one of the superuser)
*Go to terminal* \
```
psql -h localhost -p 5432 -U (user) (database name)
```

## Creating or deleting a database
```
 CREATE DATABASE name_database; 
 DROP DATABASE name_database;
 ```
 ## Moving into the database
 ```
 \c database_name
 ```
  ## Show all table into the database
 ```
 \dt
 ```
 
 ## How to create a table
 ```
 \c database_name
 CREATE TABLE table_name ( #enter
 Column_name data_type constraint_or_not,
 id BIGSERIAL NOT NULL PRIMARY KEY,
 first_name VARCHAR(50) NOT NULL,
 last_name VARCHAR(50) NOT NULL,
 date_of_birth DATE NOT NULL,
 email VARCHAR(150));
```
## How to insert record into tables
```
INSERT INTO table_name (first_name, last_nam e, gender, date_of_birth)
VALUES ('Anne', 'Smith', 'FEMALE', date '1988-01-09');
```
## How to import from a file
 ```  
 \i /Users/../../blabla.sql
 SELECT * FROM table_name;
 ```
 ## How to sort by order
 ```
 SELECT * FROM table_name ORDER BY table_section;
  ```
 
