---
layout: post
title: "Databases | Practical class 1"
description: PostgreSQL Introduction
date: 2025-02-06 08:30:00 +0500
categories: [class_materials,databases_en,practice]
---
<!-- /assets/images/2025-02-05-postgres-install -->

# PostgreSQL Introduction

# Download and Install PostgreSQL

To install PostgreSQL locally on your computer, visit the [installer by EDB](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads), and download the newest version compatible with your operating system.

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20095648%201.png)

## Start the Install

When the downloading is complete, double click the downloaded file and start the installation:

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20095922.png)

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install2.png)

## Specify Directory

You can specify the location of PostgreSQL, I will go with the default choice:

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20100145.png)

## Select Components

To use PostgreSQL, you will need to install the PostgreSQL Server. In this tutorial we will also use the pgAdmin 4 component, and the Command Line Tools:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install4.png)

## Storage Directory

You can also choose where to store the database data, I will go with the default choice:

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20100308.png)

## Select Password

You will have to select a password to get access to the database. Since this is a local database, with no incoming connection, I will choose the password 12345678:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install6.png)

## Select Port

You can set the port the server should listen on, I will go with the default choice:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install7.png)

## Select Locale

Select the geographically location of the database server:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install8.png)

## Final Check

If everything looks OK, click 'Next' to continue:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install9.png)

## Start Installation:

Click 'Next' to start the installation:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install10.png)

## Installing

This can take a while, please wait.

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install11.png)

## Complete!

Now you have installed PostgreSQL on your computer, and in the next chapter you will start using it!

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install12.png)

---
# Connect to the Database

## SQL Shell (psql)

SQL Shell (psql) is a terminal based program where you can write and execute SQL syntax in the command-line terminal.

### Open SQL Shell (psql)

You will find the SQL Shell (psql) tool in the start menu under PostgreSQL:

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20100931%201.png)

Once the program is open, you should see a window like the one below.

Insert the name of the server.

The suggested choice is localhost, which is correct, press Enter to accept:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell1.png)

## Database

The suggested database is postgres, which is correct, press Enter to accept:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell2.png)

## Port

The suggested port is 5432, which is correct, at least in my case, press Enter to accept:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell3.png)

## Username

The suggested username is postgres, which is correct, press Enter to accept:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell4.png)

## Password

Enter the password you chose when you installed the PostgreSQL database, my password is 12345678:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell5.png)

## Result

The result might look like an error, but if it shows `psql (17.2)` or any other version, and in the end you see the `postgres=#` command (and maybe a warning in between), then you have successfully connected to the database!

![](/assets/images/2025-02-05-postgres-install/Pasted%20image%2020250205133203.png)

## Execute SQL Statements

Once you have connected to the database, you can start executing SQL statements.

Our database is empty, so we cannot query any tables yet, but we can check the version with this SQL statement:

```sql
SELECT version();
```

To insert SQL statements in the SQL Shell command, just write them after the `postgres=#` command like this:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell7.png)

Press Enter and the result should look like this:

![](/assets/images/2025-02-05-postgres-install/Pasted%20image%2020250205133248.png)

## Remember the Semicolon

> Always end SQL statements with a semicolon `;`

---

# pgAdmin4

## Start pgAdmin4

You will find the pgAdmin4 application in the start menu under PostgreSQL:

![](/assets/images/2025-02-05-postgres-install/Pasted%20image%2020250205133521.png)

## pgAdmin4

Start by opening the Servers option in the menu on the left:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_2.png)

## Connect to Server

Now you need to enter the password that you created when you installed PostgreSQL, my password is 12345678:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_3.png)

## Find Database

Click on the Database option on in the menu on the left:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_4.png)

## Open Query Tool

You should find a database named `postgres`, right-click it choose the "Query Tool":

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_5.png)

## Query Tool

In the Query Tool we can start executing SQL statements.

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_6.png)

## Write SQL Statements

Our database is empty, so we cannot query any tables yet, but we can check the version with this SQL statement:

```sql
SELECT version();
```

To insert SQL statements in the Query Tool, just write in the input box like this:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_7.png)

## Execute SQL Statements

To execute a SQL statement, click the "Play" button above the input box:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_8.png)

## Result

The SQL statement is executed, and you can see the result in the "Data Output" area:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_9.png)

Now we have learned two ways of connection to a database and execute SQL statements on it:

- SQL Shell (psql)
- pgAdmin 4