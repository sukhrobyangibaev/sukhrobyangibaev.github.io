---
layout: post
title: "Databases | Final Exam"
description: Questions for Final Exam
date: 2025-05-18 00:00:01 +0500
categories: [class_materials,databases_en,lecture]
---

- Question:  Describe three key purposes of using databases in modern systems. For each purpose, briefly explain why it is important.
- Answer:
    1. **Organized and Persistent Storage:** Databases provide a structured and lasting way to store data. This is important because it allows for efficient management and retrieval of information over time, even when systems are restarted or powered down.
    2. **Efficient Data Retrieval and Manipulation:** Databases are designed for quick access and modification of data. This is crucial for applications that need to rapidly find, update, or analyze information, ensuring responsiveness and efficiency.
    3. **Maintaining Data Integrity and Consistency:** Databases enforce rules and constraints to ensure data accuracy and reliability. This is vital for trust in the data and for applications that depend on correct information for their operations.

---

- Question:  Describe three key responsibilities of a Database Administrator (DBA). Explain why each responsibility is important for the successful operation of a database system.
- Answer:
    1. **Ensuring Database Availability and Reliability:** DBAs are responsible for making sure the database is operational and accessible when needed, and that it functions correctly. This is crucial because users and applications rely on the database to be consistently available to perform their tasks.
    2. **Maintaining Data Integrity and Security:** DBAs protect data from corruption, unauthorized access, and breaches. This is vital for maintaining trust in the data and for complying with security and privacy regulations.
    3. **Optimizing Database Performance:** DBAs tune and monitor the database to ensure it runs efficiently and responds quickly to queries. This is important for user satisfaction and for the overall performance of applications that rely on the database.

---

- Question: Define the following terms in the context of the relational model and give a brief example for each using a "Products" table with attributes (ProductID, ProductName, Price, Category): Relation, Attribute, Tuple, Domain.
- Answer:
    - **Relation:** A *relation* is a table with rows and columns. In our "Products" example, the entire "Products" table itself is a relation.
    - **Attribute:** An *attribute* is a named column of a relation. Examples in the "Products" table are: ProductID, ProductName, Price, and Category.
    - **Tuple:** A *tuple* is a row in a relation, representing a single record.  An example tuple in the "Products" table would be a single product entry, like (1, 'Laptop', 1200, 'Electronics').
    - **Domain:** A *domain* is the set of permissible values for an attribute. For the "Price" attribute in "Products," the domain might be positive decimal numbers. For "Category," the domain could be a set of strings like {'Electronics', 'Books', 'Clothing', ...}.

---

- Question: Outline the stages of the database lifecycle in a Waterfall model. Briefly describe the primary activity in each stage. 
- Answer:
    *   **Planning:** Initial stage defining project scope, goals, and feasibility.
    *   **Requirements Gathering:**  Collecting and documenting user needs and data requirements through interviews, questionnaires, etc.
    *   **Conceptual Design:** Creating a high-level, abstract model (like an ER diagram) of the database structure.
    *   **Logical Design:** Translating the conceptual model into a specific database schema, often using the relational model (defining tables, columns, data types).
    *   **Physical Design:**  Determining physical storage structures, indexing strategies, and access paths for optimal performance.
    *   **Implementation:** Building the database using a DBMS, creating the database objects and loading initial data.
    *   **Testing:** Verifying the database functionality, performance, and data integrity.
    *   **Deployment:**  Making the database operational and accessible to users.
    *   **Maintenance and Evolution:**  Ongoing monitoring, performance tuning, updates, and adapting to changing requirements.

---

- Question:  Briefly describe *three* key skills that are essential for a Database Administrator (DBA) to be effective in their role.
- Answer:
    1.  **Technical Skills:** DBAs require strong technical skills in Database Management Systems (DBMS), SQL, operating systems, and related technologies. These technical skills are fundamental for tasks like database installation, configuration, performance tuning, security implementation, and troubleshooting.
    2.  **Problem-Solving and Analytical Abilities:** DBAs frequently encounter complex technical issues and performance bottlenecks. Strong problem-solving and analytical skills are essential to diagnose problems, identify root causes, and develop effective solutions to ensure database stability and optimal performance.
    3.  **Communication and Collaboration Skills:** DBAs need to communicate effectively with various stakeholders, including developers, users, and management. They must be able to explain technical concepts clearly, gather requirements, and collaborate with teams to ensure the database meets organizational needs.

---

- Question:  Describe the purpose of using indexes in databases. Explain the difference between a primary index and a secondary index.
- Answer: Indexes in databases are used to **improve the efficiency of data retrieval**. They are separate structures that map data values to their physical locations, allowing the database to quickly locate records without scanning the entire table.
    - **Primary Index:**  An index based on the **primary key** of a table. It is used to enforce uniqueness and provide fast access to records based on the primary key value. There is typically only one primary index per table.
    - **Secondary Index:** An index created on **non-primary key attributes** (columns). Secondary indexes provide faster access to records based on these attributes, enabling efficient querying on different criteria beyond the primary key.  A table can have multiple secondary indexes.

---

- Question: Describe the CIA Triad in the context of database security. For each component (Confidentiality, Integrity, Availability), explain its meaning and importance for securing a database system.
- Answer: The **CIA Triad** is a fundamental model that guides information security policies and practices, including database security. It stands for:
    - **Confidentiality:** Ensuring that data is accessible only to authorized users and preventing unauthorized disclosure. *Importance:* Protects sensitive information from being leaked or exposed to those who should not have access, maintaining privacy and trust.
    - **Integrity:** Maintaining the accuracy and completeness of data, and preventing unauthorized modification or corruption. *Importance:* Ensures that data is reliable and trustworthy for decision-making and application functionality. Data corruption can lead to incorrect operations and loss of confidence in the system.
    - **Availability:** Ensuring that authorized users have reliable and timely access to data and resources when needed. *Importance:*  Guarantees that the database system is operational and accessible for legitimate users to perform their tasks. Loss of availability can disrupt business operations and services.

---

- Question:  SQL is categorized into four core functions: DDL, DML, DCL, and DQL. Briefly define each of these and state their main purpose.
- Answer:
    *   **DDL (Data Definition Language):** Used to **define and modify the database structure**.  It includes commands for creating, altering, and dropping database objects like tables.
    *   **DML (Data Manipulation Language):** Used to **manipulate the data within the database**. It includes commands for inserting, updating, deleting, and retrieving data.
    *   **DCL (Data Control Language):** Used to **control access and permissions** within the database. It includes commands for granting and revoking privileges to users.
    *   **DQL (Data Query Language):** Focused on the **retrieval of data from the database**. The primary command is `SELECT`, used to query and fetch data based on specified criteria.

---

- Question:  What is the difference between Interactive SQL and Embedded SQL?  Give an example scenario where each would be typically used.
- Answer:
    *   **Interactive SQL:**  SQL statements are executed **directly through a database client** (like a command-line tool or GUI). It's used for ad-hoc queries, database administration tasks, and data exploration.
    *   *Example Scenario:* A database administrator using a command-line tool to check the current number of records in a table.
    *   **Embedded SQL:** SQL statements are **integrated within the source code of an application** (e.g., Java, Python). The application code executes these SQL queries to interact with the database. It is used for building database-driven applications and dynamic data retrieval.
    *   *Example Scenario:* A web application written in Python that retrieves product information from a database to display on a webpage.

---

- Question: List and briefly describe the main stages of the database design lifecycle, in the correct order.
- Answer:
    1. **Requirements Analysis and Specification:** Understanding user needs and defining the data requirements, including entities, attributes, relationships, and business rules.
    2. **Conceptual Design:** Creating a high-level, abstract model (often using ER diagrams) that is DBMS-independent.
    3. **Logical Design:** Translating the conceptual model into a specific database schema based on a chosen data model (e.g., relational), defining tables, columns, data types, and relationships.
    4. **Physical Design:** Determining physical storage structures, access paths, file organization, and indexing techniques to optimize performance.
    5. **Implementation and Deployment:** Building the database using a DBMS, creating tables, defining constraints, loading data, and making it operational for users.
    6. **Maintenance and Evolution:** Ongoing monitoring, performance tuning, applying updates, and adapting to changing requirements over time.

---

- Question: Describe the Three-Tier Architecture of a database system. Explain the purpose of each tier (External, Conceptual, and Physical) and how this architecture promotes data independence.
- Answer: The Three-Tier Architecture divides a database system into three distinct levels to enhance data independence and organization:
    1. **External Tier (View Level / Presentation Level):** This is the user-facing tier, providing customized views of the database tailored to specific user groups or applications. Users interact with the database through interfaces at this level. *Purpose:* To simplify user interaction, customize data presentation, and enhance security by limiting data access to specific views.
    2. **Conceptual Tier (Logical Level):** This tier represents the overall logical structure of the database, defining what data is stored and the relationships between data entities. It is independent of both physical storage and user views. *Purpose:* To provide a unified and abstract view of the data, independent of physical implementation, and to facilitate database design and understanding.
    3. **Physical Tier (Internal Level / Storage Level):** This tier deals with the physical storage of data on storage media, including file organization, indexing, and storage formats. *Purpose:* To manage the physical storage of data efficiently, optimize performance, and handle storage-level security.

---

- Question:  Explain the difference between "Physical Data Description" and "Logical Data Description" in the context of database architecture. Give an example of each type of description for a table named "Customers" with columns "CustomerID", "Name", and "Address".
- Answer:
    - **Physical Data Description:**  Details *how* data is actually stored on physical storage. It focuses on the implementation aspects of data storage. *Example for "Customers" table:*
        - The "Customers" table data is stored in a file named "customer_data.dat" on disk, using sequential file organization.
        - Indexes are created on "CustomerID" using a B-tree index structure for faster lookups.
        - Data types are stored as VARCHAR for "Name" and "Address" with a maximum length of 255 characters, and INTEGER for "CustomerID".
    - **Logical Data Description:** Focuses on *what* data is stored, its structure, and relationships, as perceived by users and developers. It's about the meaning and organization of data, independent of physical storage. *Example for "Customers" table:*
        - The "Customers" table entity has attributes: "CustomerID" (primary key, integer), "Name" (string), and "Address" (string).
        - "CustomerID" uniquely identifies each customer.
        - There is no explicit relationship defined with other entities at this level, but conceptually, a customer may be related to "Orders" in another table.

---

- Question:  Describe the roles of the following three key components of a Database Management System (DBMS): Storage Manager, Query Processor, and Transaction Manager. Briefly explain how each component contributes to the overall functionality of the DBMS.
- Answer:
    1. **Storage Manager:** *Role:* Manages the physical storage of data on disk. *Contribution:* It is responsible for efficient data access, file organization, buffering data in memory, and enforcing authorization and integrity constraints at the physical level. It ensures data is stored and retrieved effectively and securely.
    2. **Query Processor:** *Role:* Processes user queries (typically SQL). *Contribution:* It takes user queries, parses and validates them, optimizes query execution plans, and then executes these plans to retrieve or modify data. It translates user requests into operations that the Storage Manager can perform, bridging the gap between user requests and physical data storage.
    3. **Transaction Manager:** *Role:* Ensures reliable processing of database transactions and guarantees ACID properties. *Contribution:* It manages concurrency by controlling simultaneous transactions and ensures data consistency and integrity. It also handles recovery management to restore the database to a consistent state after system failures, ensuring that transactions are processed reliably and data is protected against failures.

---

- Question:  Explain the differences between a Superkey, a Candidate Key, and a Primary Key.  Using the "Students" table (StudentID, Name, Email, Major, Phone), identify one example of each type of key. Assume StudentID and Email are unique for each student.
- Answer:
    - **Superkey:** A *superkey* is any attribute or set of attributes that uniquely identifies a tuple in a relation. Example in "Students": {StudentID, Name}, {Email, Phone}, {StudentID, Name, Email, Major, Phone}.
    - **Candidate Key:** A *candidate key* is a minimal superkey. It is a superkey such that no proper subset of it is also a superkey. Examples in "Students": {StudentID}, {Email}.
    - **Primary Key:** A *primary key* is one of the candidate keys chosen to be the main identifier for the relation. It is chosen for convenience and efficiency.  In "Students", we might choose **StudentID** as the primary key.

---

- Question:  Categorize the following Relational Algebra operations as either Unary or Binary and briefly explain why: SELECT (σ), PROJECT (π), UNION (∪), CARTESIAN PRODUCT (×).
- Answer:
    - **Unary Operations:**
        - **SELECT (σ):** Unary because it operates on a single relation, filtering rows based on a condition.
        - **PROJECT (π):** Unary because it operates on a single relation, selecting specific columns.
    - **Binary Operations:**
        - **UNION (∪):** Binary because it combines tuples from *two* relations.
        - **CARTESIAN PRODUCT (×):** Binary because it combines tuples from *two* relations to produce all possible pairs.

---

- Question:
    You are given two tables: `Products` (with columns `product_id INT`, `product_name VARCHAR(255)`, `category_id INT`, `price DECIMAL(10,2)`) and `Categories` (with columns `category_id INT`, `category_name VARCHAR(100)`).
    Write an SQL query to retrieve the name of each category and the total number of products belonging to that category. The results should be ordered by the number of products in descending order. Display `category_name` and `product_count`.
-   Answer:
    ```sql
    SELECT
        c.category_name,
        COUNT(p.product_id) AS product_count
    FROM
        Categories c
    JOIN
        Products p ON c.category_id = p.category_id
    GROUP BY
        c.category_name
    ORDER BY
        product_count DESC;
    ```

---

- Question:
    Consider a database with two tables: `Books` (columns: `book_id INT`, `title VARCHAR(255)`, `author_id INT`, `pages INT`) and `Authors` (columns: `author_id INT`, `author_name VARCHAR(100)`).
    Write an SQL query to calculate the average number of pages for books written by each author. Only include authors whose average book page count is greater than 300. Display the `author_name` and their `average_pages`, ordered by `average_pages` in descending order.
-   Answer:
    ```sql
    SELECT
        a.author_name,
        AVG(b.pages) AS average_pages
    FROM
        Authors a
    JOIN
        Books b ON a.author_id = b.author_id
    GROUP BY
        a.author_name
    HAVING
        AVG(b.pages) > 300
    ORDER BY
        average_pages DESC;
    ```

---

- Question:
    You have access to an `Employees` table (columns: `employee_id INT`, `first_name VARCHAR(50)`, `department_id INT`, `hire_date DATE`, `salary DECIMAL(10,2)`) and a `Departments` table (columns: `department_id INT`, `department_name VARCHAR(100)`).
    Write an SQL query to list all departments that have more than 5 employees who were hired on or after '2023-01-01'. For each such department, display its `department_name` and the `num_recent_employees` (the count of these recently hired employees). The results should be ordered alphabetically by `department_name`.
-   Answer:
    ```sql
    SELECT
        d.department_name,
        COUNT(e.employee_id) AS num_recent_employees
    FROM
        Departments d
    JOIN
        Employees e ON d.department_id = e.department_id
    WHERE
        e.hire_date >= '2023-01-01'
    GROUP BY
        d.department_name
    HAVING
        COUNT(e.employee_id) > 5
    ORDER BY
        d.department_name ASC;
    ```

---

- Question:
    A company tracks sales data in a `Sales` table (columns: `sale_id INT`, `product_id INT`, `sale_date DATE`, `quantity_sold INT`, `unit_price DECIMAL(10,2)`) and product information in a `ProductsInfo` table (columns: `product_id INT`, `product_name VARCHAR(255)`, `category VARCHAR(50)`).
    Write an SQL query to calculate the total revenue (defined as `quantity_sold * unit_price`) generated by each product `category`. Only include categories for which the total revenue is greater than $5,000. Display the `category` and its `total_revenue`. The results should be ordered by `total_revenue` in descending order.
-   Answer:
    ```sql
    SELECT
        pi.category,
        SUM(s.quantity_sold * s.unit_price) AS total_revenue
    FROM
        Sales s
    JOIN
        ProductsInfo pi ON s.product_id = pi.product_id
    GROUP BY
        pi.category
    HAVING
        SUM(s.quantity_sold * s.unit_price) > 5000.00
    ORDER BY
        total_revenue DESC;
    ```

---

- Question:
    Given tables `BranchA_Customers` (`customer_id INT`, `name VARCHAR`) and `BranchB_Customers` (`customer_id INT`, `name VARCHAR`), list the `customer_id` and `name` of all unique customers present in *either* branch.
    Answer:
    ```sql
    SELECT customer_id, name
    FROM BranchA_Customers
    UNION
    SELECT customer_id, name
    FROM BranchB_Customers
    ORDER BY customer_id;
    ```

---

- Question:
    You have two tables: `Morning_Shift_Logins` (`employee_id INT`, `login_time TIMESTAMP`) and `Evening_Shift_Logins` (`employee_id INT`, `login_time TIMESTAMP`). Retrieve the `employee_id` of employees who logged in during *both* the morning shift and the evening shift.
    Answer:
    ```sql
    SELECT employee_id
    FROM Morning_Shift_Logins
    INTERSECT
    SELECT employee_id
    FROM Evening_Shift_Logins
    ORDER BY employee_id;
    ```

---

- Question:
    Consider tables `All_Subscribers` (`email VARCHAR PRIMARY KEY`, `join_date DATE`) and `Unsubscribed_Users` (`email VARCHAR PRIMARY KEY`, `unsubscribe_date DATE`). List the `email` of subscribers who are in `All_Subscribers` but *not* in `Unsubscribed_Users`.
    Answer:
    ```sql
    SELECT email
    FROM All_Subscribers
    EXCEPT
    SELECT email
    FROM Unsubscribed_Users
    ORDER BY email;
    ```

---

- Question:
    Two event guest lists are stored in `Event1_Attendees` (`guest_name VARCHAR`, `email VARCHAR`) and `Event2_Attendees` (`guest_name VARCHAR`, `email VARCHAR`). Produce a combined list of `guest_name` and `email` from both events. If a person attended both events, they should appear twice in the result.
    Answer:
    ```sql
    SELECT guest_name, email
    FROM Event1_Attendees
    UNION ALL
    SELECT guest_name, email
    FROM Event2_Attendees;
    ```

---

- Question:
    You have two tables: `Employees` (columns: `employee_id INT PRIMARY KEY`, `employee_name VARCHAR(100)`, `department_id INT`) and `Departments` (columns: `department_id INT PRIMARY KEY`, `department_name VARCHAR(100)`).
    Write a PostgreSQL query to retrieve the `employee_name` and the `department_name` for all employees who are assigned to a department.
-   Answer:
    ```sql
    SELECT E.employee_name, D.department_name
    FROM Employees E
    INNER JOIN Departments D ON E.department_id = D.department_id;
    ```

---

- Question:
    Consider the tables: `Books` (columns: `book_id INT PRIMARY KEY`, `title VARCHAR(255)`, `author_id INT`) and `Authors` (columns: `author_id INT PRIMARY KEY`, `author_name VARCHAR(100)`).
    Write a PostgreSQL query to list the `title` of all books and their corresponding `author_name`. Include books that may not have a matching author in the `Authors` table (display NULL for `author_name` in such cases).
-   Answer:
    ```sql
    SELECT B.title, A.author_name
    FROM Books B
    LEFT JOIN Authors A ON B.author_id = A.author_id;
    ```

---

- Question:
    Given three tables: `Students` (columns: `student_id INT PRIMARY KEY`, `student_name VARCHAR(100)`), `Enrollments` (columns: `enrollment_id INT PRIMARY KEY`, `student_id INT`, `course_id INT`), and `Courses` (columns: `course_id INT PRIMARY KEY`, `course_name VARCHAR(100)`, `credits INT`).
    Write a PostgreSQL query to display the `student_name`, `course_name`, and `credits` for every course a student is enrolled in. Only include students who are enrolled in at least one course.
-   Answer:
    ```sql
    SELECT S.student_name, C.course_name, C.credits
    FROM Students S
    INNER JOIN Enrollments E ON S.student_id = E.student_id
    INNER JOIN Courses C ON E.course_id = C.course_id;
    ```


---


- Question: 
The `Staff` table has columns: `staff_id INT`, `first_name VARCHAR(50)`, `last_name VARCHAR(50)`. Write a query to display `staff_id`, the full name (concatenation of `first_name`, a space, and `last_name`), and an email prefix. The email prefix must be the first letter of `first_name` followed by `last_name`, all in lowercase. For example, for 'Ada' and 'Lovelace', the email prefix is 'alovelace'.
-   Answer:
    ```sql
    SELECT
        staff_id,
        first_name || ' ' || last_name AS full_name,
        LOWER(SUBSTRING(first_name FROM 1 FOR 1) || last_name) AS email_prefix
    FROM Staff;
    ```

---

- Question:
 The `EventLog` table contains: `log_id INT`, `event_name VARCHAR(100)`, `event_time TIMESTAMP`. Retrieve the `event_name`, the `event_time` formatted as 'DD/MM/YYYY HH24:MI' (e.g., '31/12/2023 23:59'), and the full name of the day of the week (e.g., 'Tuesday', trimmed of any padding) extracted from `event_time`.
-   Answer:
    ```sql
    SELECT
        event_name,
        TO_CHAR(event_time, 'DD/MM/YYYY HH24:MI') AS formatted_event_time,
        TRIM(TO_CHAR(event_time, 'Day')) AS day_of_week
    FROM EventLog;
    ```

---

- Question:
 The `Projects` table is defined as: `project_id INT`, `project_name VARCHAR(100)`, `start_date DATE`, `duration_days INT`. Calculate and list the `project_name`, its `start_date`, and its `estimated_end_date`. The `estimated_end_date` is derived by adding `duration_days` (as days) to the `start_date`.
-   Answer:
    ```sql
    SELECT
        project_name,
        start_date,
        start_date + (duration_days * INTERVAL '1 day') AS estimated_end_date
    FROM Projects;
    ```

---

- Question:
 Given the `SensorReadings` table (`reading_id INT`, `sensor_name VARCHAR(50)`, `temperature_celsius DECIMAL(5,2)`, `humidity_percentage DECIMAL(5,2)` where `humidity_percentage` can be `NULL`), display the `sensor_name`, `temperature_celsius` rounded to one decimal place, and `humidity_percentage`. If `humidity_percentage` is `NULL`, it should be displayed as 0.0.
-   Answer:
    ```sql
    SELECT
        sensor_name,
        ROUND(temperature_celsius, 1) AS rounded_temperature,
        COALESCE(humidity_percentage, 0.0) AS adjusted_humidity
    FROM SensorReadings;
    ```

---

- Question:
 Write an SQL query using the `Employees` table (columns: `employee_id INT`, `department_id INT`, `salary DECIMAL(10,2)`) and the `Departments` table (columns: `department_id INT`, `department_name VARCHAR(100)`). Retrieve each `department_name` and its average employee `salary`. The average salary column should be named `avg_salary`.
-   Answer:
    ```sql
    SELECT
        d.department_name,
        AVG(e.salary) AS avg_salary
    FROM
        Employees e
    JOIN
        Departments d ON e.department_id = d.department_id
    GROUP BY
        d.department_name;
    ```

---

- Question:
 Using the `Products` table (columns: `product_id INT`, `category_id INT`) and the `Categories` table (columns: `category_id INT`, `category_name VARCHAR(100)`), list each `category_name` and the total number of products within it. Name the count column `product_count`.
-   Answer:
    ```sql
    SELECT
        c.category_name,
        COUNT(p.product_id) AS product_count
    FROM
        Products p
    JOIN
        Categories c ON p.category_id = c.category_id
    GROUP BY
        c.category_name;
    ```

---

- Question: 
From the `OrderItems` table (columns: `order_item_id INT`, `product_id INT`, `quantity INT`) and the `Products` table (columns: `product_id INT`, `product_name VARCHAR(255)`), calculate the total `quantity` sold for each `product_name`. Display the `product_name` and the calculated sum as `total_quantity_sold`.
-   Answer:
    ```sql
    SELECT
        pr.product_name,
        SUM(oi.quantity) AS total_quantity_sold
    FROM
        OrderItems oi
    JOIN
        Products pr ON oi.product_id = pr.product_id
    GROUP BY
        pr.product_name;
    ```

---

- Question:
 For each department, determine the minimum and maximum employee salaries. Use the `Employees` table (columns: `employee_id INT`, `department_id INT`, `salary DECIMAL(10,2)`) and the `Departments` table (columns: `department_id INT`, `department_name VARCHAR(100)`). Display the `department_name`, `min_salary`, and `max_salary`.
-   Answer:
    ```sql
    SELECT
        d.department_name,
        MIN(e.salary) AS min_salary,
        MAX(e.salary) AS max_salary
    FROM
        Employees e
    JOIN
        Departments d ON e.department_id = d.department_id
    GROUP BY
        d.department_name;
    ```

---

- Question: From `Employees` (columns: `employee_id INT`, `first_name VARCHAR(50)`, `last_name VARCHAR(50)`, `department_id INT`) and `Departments` (columns: `department_id INT`, `department_name VARCHAR(100)`), retrieve each `department_name`. For each department, also provide a comma-separated list of employee full names (formatted as 'FirstName LastName'). Name this list column `employee_list`. Order the results by `department_name`.
-   Answer:
    ```sql
    SELECT
        d.department_name,
        STRING_AGG(e.first_name || ' ' || e.last_name, ', ') AS employee_list
    FROM
        Employees e
    JOIN
        Departments d ON e.department_id = d.department_id
    GROUP BY
        d.department_name
    ORDER BY
        d.department_name;
    ```

---


- Question:
    Write an SQL query to list the first name, last name, and department name for all employees.
    You will need to use the `Employees` table (columns: `employee_id INT`, `first_name VARCHAR(100)`, `last_name VARCHAR(100)`, `department_id INT`) and the `Departments` table (columns: `department_id INT`, `department_name VARCHAR(100)`). Join them on their common `department_id`. Display `first_name`, `last_name`, and `department_name`.
-   Answer:
    ```sql
    SELECT
        e.first_name,
        e.last_name,
        d.department_name
    FROM
        Employees e
    INNER JOIN
        Departments d ON e.department_id = d.department_id;
    ```

---

- Question:
    Write an SQL query to retrieve the names of customers and the dates of all orders they have placed.
    Use the `Customers` table (columns: `customer_id INT`, `customer_name VARCHAR(255)`) and the `Orders` table (columns: `order_id INT`, `customer_id INT`, `order_date DATE`). Join them using `customer_id`. Display `customer_name` and `order_date`.
-   Answer:
    ```sql
    SELECT
        c.customer_name,
        o.order_date
    FROM
        Customers c
    INNER JOIN
        Orders o ON c.customer_id = o.customer_id;
    ```

---

- Question:
    Write an SQL query to list student names and the names of courses they are currently enrolled in.
    Use `Students` (columns: `student_id INT`, `student_name VARCHAR(150)`), `Enrollments` (columns: `enrollment_id INT`, `student_id INT`, `course_id INT`), and `Courses` (columns: `course_id INT`, `course_name VARCHAR(200)`). You will need to join `Students` to `Enrollments` on `student_id`, and `Enrollments` to `Courses` on `course_id`. Display `student_name` and `course_name`.
-   Answer:
    ```sql
    SELECT
        s.student_name,
        c.course_name
    FROM
        Students s
    INNER JOIN
        Enrollments e ON s.student_id = e.student_id
    INNER JOIN
        Courses c ON e.course_id = c.course_id;
    ```

---

- Question:
    Write an SQL query to find the names of products and the quantity sold for all orders placed specifically on '2023-10-26'.
    Use `Products` (columns: `product_id INT`, `product_name VARCHAR(255)`), `OrderItems` (columns: `order_item_id INT`, `order_id INT`, `product_id INT`, `quantity INT`), and `Orders` (columns: `order_id INT`, `order_date DATE`). Join `Orders` with `OrderItems` on `order_id`, and `OrderItems` with `Products` on `product_id`. Filter results where `order_date` is '2023-10-26'. Display `product_name` and `quantity`.
-   Answer:
    ```sql
    SELECT
        p.product_name,
        oi.quantity
    FROM
        Orders o
    INNER JOIN
        OrderItems oi ON o.order_id = oi.order_id
    INNER JOIN
        Products p ON oi.product_id = p.product_id
    WHERE
        o.order_date = '2023-10-26';
    ```

---

- Question:
    Write an SQL query to list book titles and the names of their authors, but only for authors whose nationality is 'British'.
    Use `Books` (columns: `book_id INT`, `title VARCHAR(255)`), `BookAuthors` (columns: `book_id INT`, `author_id INT`), and `Authors` (columns: `author_id INT`, `author_name VARCHAR(150)`, `nationality VARCHAR(100)`). Join `Books` with `BookAuthors` on `book_id`, and `BookAuthors` with `Authors` on `author_id`. Filter results where `nationality` is 'British'. Display `title` and `author_name`.
-   Answer:
    ```sql
    SELECT
        b.title,
        a.author_name
    FROM
        Books b
    INNER JOIN
        BookAuthors ba ON b.book_id = ba.book_id
    INNER JOIN
        Authors a ON ba.author_id = a.author_id
    WHERE
        a.nationality = 'British';
    ```

---

- Question:
    You have a table `Employees` with columns: `employee_id INT PRIMARY KEY`, `full_name VARCHAR(100)`, `department VARCHAR(50)`, `job_title VARCHAR(50)`, and `salary DECIMAL(10,2)`.
    Create a PostgreSQL VIEW named `HighSalariedTechStaffView`. This view should display the `full_name`, `job_title`, and `salary` of all employees who work in the 'Technology' department and earn more than 75000.
-   Answer:
    ```sql
    CREATE VIEW HighSalariedTechStaffView AS
    SELECT full_name, job_title, salary
    FROM Employees
    WHERE department = 'Technology' AND salary > 75000;
    ```

---

- Question:
    Consider a table `Products` with columns: `product_id INT PRIMARY KEY`, `product_name VARCHAR(100)`, `category VARCHAR(50)`, `unit_price DECIMAL(8,2)`, and `stock_level INT`.
    Create a PostgreSQL VIEW named `LowStockElectronicsView`. This view should show `product_id`, `product_name`, and `stock_level` for products in the 'Electronics' category where the `stock_level` is below 20.
-   Answer:
    ```sql
    CREATE VIEW LowStockElectronicsView AS
    SELECT product_id, product_name, stock_level
    FROM Products
    WHERE category = 'Electronics' AND stock_level < 20;
    ```

---

- Question:
    You have three tables:
    `Students` (`student_id INT PRIMARY KEY`, `student_name VARCHAR(100)`, `major VARCHAR(50)`)
    `Courses` (`course_id INT PRIMARY KEY`, `course_name VARCHAR(100)`, `department VARCHAR(50)`)
    `Enrollments` (`enrollment_id INT PRIMARY KEY`, `student_id INT REFERENCES Students(student_id)`, `course_id INT REFERENCES Courses(course_id)`, `enrollment_date DATE`)
    Create a PostgreSQL VIEW named `CSStudentEnrollmentsView`. This view should list `student_name` (from `Students`) and `course_name` (from `Courses`) for all students enrolled in courses offered by the 'Computer Science' department.
-   Answer:
    ```sql
    CREATE VIEW CSStudentEnrollmentsView AS
    SELECT s.student_name, c.course_name
    FROM Students s
    JOIN Enrollments e ON s.student_id = e.student_id
    JOIN Courses c ON e.course_id = c.course_id
    WHERE c.department = 'Computer Science';
    ```

---

- Question:
    Given a table `BookSales` with columns: `sale_id INT PRIMARY KEY`, `book_title VARCHAR(150)`, `quantity_sold INT`, `price_per_unit DECIMAL(6,2)`, `sale_date DATE`.
    Create a PostgreSQL VIEW named `BookSaleRevenueView`. This view should display `sale_id`, `book_title`, `sale_date`, and a calculated column `total_revenue` (as `quantity_sold * price_per_unit`) for each sale.
-   Answer:
    ```sql
    CREATE VIEW BookSaleRevenueView AS
    SELECT sale_id, book_title, sale_date, (quantity_sold * price_per_unit) AS total_revenue
    FROM BookSales;
    ```

---

- Question:
    You have a table `ProjectTasks` with columns: `task_id INT PRIMARY KEY`, `project_name VARCHAR(100)`, `task_description TEXT`, `assignee VARCHAR(50)`, `due_date DATE`, `status VARCHAR(20)`. Assume `CURRENT_DATE` can be used to get today's date.
    Create a PostgreSQL VIEW named `OverdueProjectTasksView`. This view should list `project_name`, `task_description`, `assignee`, and `due_date` for all tasks where the `status` is NOT 'Completed' and the `due_date` is before `CURRENT_DATE`.
-   Answer:
    ```sql
    CREATE VIEW OverdueProjectTasksView AS
    SELECT project_name, task_description, assignee, due_date
    FROM ProjectTasks
    WHERE status != 'Completed' AND due_date < CURRENT_DATE;
    ```