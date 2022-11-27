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
