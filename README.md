# Enhancing System Security with SQL Queries

## Project Overview

This project focuses on enhancing system security and managing employee machines through advanced SQL queries. The main goal is to optimize security measures and efficiently handle data management.

## SQL Queries Used

### 1. Retrieve After Hours Failed Login Attempts
This query filters for failed login attempts that occurred after 18:00.

![1](https://github.com/user-attachments/assets/58f3da37-3fc6-4400-90ad-4915b172fab5)

This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. The first condition is login_time > '18:00', which filters for the login attempts that occurred after 18:00. The second condition is success = FALSE, which filters for the failed login attempts.


### 2. Retrieve Login Attempts on Specific Dates
This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08.

![2](https://github.com/user-attachments/assets/ebf73fa8-e8c4-4ef6-ada1-53c71612fb52)

This query filters for login attempts that occurred on either 2022-05-09 or 2022-05-08. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is login_date = '2022-05-09', which filters for logins on 2022-05-09. The second condition is login_date = '2022-05-08', which filters for logins on 2022-05-08.

### 3. Retrieve Login Attempts Outside of Mexico
This query filters for login attempts that occurred in countries other than Mexico.

![3](https://github.com/user-attachments/assets/d10dc2fd-323c-4bcc-bb79-49f2e01cc3ff)

This query returns all login attempts that occurred in countries other than Mexico. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with NOT to filter for countries other than Mexico. I used LIKE with MEX% as the pattern to match because the dataset represents Mexico as MEX and MEXICO. The percentage sign (%) represents any number of unspecified characters when used with LIKE.

### 4. Retrieve Employees in Marketing
This query filters for employees in the Marketing department located in the East building.

![4](https://github.com/user-attachments/assets/da22456b-504f-449c-bada-3567e9d2ba95)

This query returns all employees in the Marketing department in the East building. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with AND to filter for employees who work in the Marketing department and in the East building. I used LIKE with East% as the pattern to match because the data in the office column represents the East building with the specific office number. The first condition is department = 'Marketing', which filters for employees in the Marketing department. The second condition is office LIKE 'East%', which filters for employees in the East building.

### 5. Retrieve Employees in Finance or Sales
This query filters for employees in the Finance or Sales departments.

![5](https://github.com/user-attachments/assets/c9633bf3-9ae9-4bb1-8647-19456255dbac)

This query returns all employees in the Finance and Sales departments. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with OR to filter for employees who are in the Finance or Sales departments. I used the OR operator instead of AND because I want all employees who are in either department. The first condition is department = 'Finance', which filters for employees from the Finance department. The second condition is department = 'Sales', which filters for employees from the Sales department.

### 6. Retrieve All Employees Not in IT
This query filters for employees who are not in the Information Technology department.

![6](https://github.com/user-attachments/assets/fd55612e-3660-4970-a41c-ccaddd79efbf)

This query returns all employees not in the Information Technology department. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with NOT to filter for employees not in this department.

## Summary
I applied filters to SQL queries to get specific information on login attempts and employee machines. I used two different tables, log_in_attempts and employees. I used the AND, OR, and NOT operators to filter for the specific information needed for each task. I also used LIKE and the percentage sign (%) wildcard to filter for patterns.

Created by Bugra (Me). Feel free to explore the project and connect with me for further discussions!

