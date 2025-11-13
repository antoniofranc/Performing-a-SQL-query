# Filter a SQL query

## Scenario
In this scenario, you need to get specific information about employees, their machines, and the departments they’re in. Your team needs this data to perform various tasks, such as running updates, posting a privacy notice in certain departments, and sending an alert to an employee with an issue on a machine.

You are responsible for finding the required information by querying a database. You’ll add filters to your queries to locate the information more quickly.

Here’s how you’ll do this task: First, you’ll list all organization machines and their operating systems. Second, you’ll list all machines with the operating system OS 2. Third, you’ll list all the employees in the Finance and Sales departments. Fourth, you’ll obtain information about machines.

## Task 1. List all organization machines
In this task, you need to get a list of all organization machines and their operating systems. The data is contained in the `machines` table. You’ll need to use the `SELECT` keyword to return specific columns.

Run a SQL query to retrieve only the `device_id` and `operating_system` columns from the `machines` table.
How many rows were returned from the machines table? (You can view the number of rows at the bottom of the output.)
<img width="655" height="380" alt="image" src="https://github.com/user-attachments/assets/5ab8b016-22f9-4303-b93e-2de7382d6d16" />
<img width="338" height="215" alt="image" src="https://github.com/user-attachments/assets/2fc71dfb-f64c-494a-b0df-a8d619c41ea3" />

---
## Task 2. Retrieve a list of the machines with OS 2
In this task, you need to obtain a list of all machines with the `'OS 2'` operating system because these machines need an update. To get this information, you’ll run your first SQL query with a filter.
- Select all the records from the `machines` table with a value of `'OS 2'` in the `operating_system` column:
SELECT device_id, operating_system 
FROM machines 
WHERE operating_system = 'OS 2';

<img width="527" height="329" alt="image" src="https://github.com/user-attachments/assets/77ebaa68-0c09-416e-8a2e-41175e99fc7c" />
<img width="451" height="84" alt="image" src="https://github.com/user-attachments/assets/d8347a88-afed-4177-ad0b-cb2a6694be10" />

---
## Task 3. List employees in specific departments

In this task, you need to retrieve a list of all the employees in the Finance and Sales departments to obtain their office numbers. A notice about handling confidential financial information will be posted to these offices.

1. Filter the rows returned from `department` column in the `employees` table to include only employees from the `'Finance'` department:
SELECT * 
FROM employees 
WHERE department = 'Finance';

What is the employee_id of the first row returned?
<img width="603" height="514" alt="image" src="https://github.com/user-attachments/assets/f947fad0-10ed-493f-b8d3-8259e6c993bc" />

2.Modify the previous query so that it returns employees who are in the 'Sales' department.

SELECT * 
FROM employees 
WHERE department = 'Sales';

<img width="607" height="695" alt="image" src="https://github.com/user-attachments/assets/08ac3fb5-f2fa-4dd8-919d-c9da53643f31" />

------
# Task 4. Identify employee machines
Your team recently discovered that there are issues with machines in the South building. In this task, you need to obtain certain employee and computer information.

A machine in `'South-109'` has an issue. You need to determine which employee uses that computer so you can send them an alert.

1. Write a query to identify which employee uses the `office` in `'South-109'`. (The data must be returned from the office column in the `employees` table.)
SELECT * 
FROM employees 
WHERE office = 'South-109';

Which of the following employees uses the computer with the issue?
<img width="601" height="208" alt="image" src="https://github.com/user-attachments/assets/ddd2c0ca-93f6-4394-a734-616393da7004" />

Next, your team has determined that there is an issue with all the machines in the South building. Offices in the organization are named with the building name, a hyphen, and the office number in that building (for example, `'South-109'`).

2. Modify the query you used in the previous step so that it returns information on all the employees in the `'South'` building. Use the `LIKE` operator with % in this query.
SELECT * 
FROM employees 
WHERE office LIKE 'South%';

Which department does the first employee listed in the South building belong to?
<img width="710" height="290" alt="image" src="https://github.com/user-attachments/assets/a9a523b4-8d0a-4fba-9d2b-82dcf4ce569c" />


