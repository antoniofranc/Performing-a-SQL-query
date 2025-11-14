# Complete a SQL join 


## Scenario 
In this scenario, you’ll investigate a recent security incident that compromised some machines.

You are responsible for getting the required information from the database for the investigation.

Here’s how you’ll do this task: `First`, you’ll use an inner join to identify which employees are using which machines. `Second`, you’ll use left and right joins to find machines that do not belong to any specific user and users who do not have any specific machine assigned to them. `Finally`, you’ll use an inner join to list all login attempts made by all employees.

-----
# Task 1. Match employees to their machines
First, you must identify which employees are using which machines. The data is located in the `machines` and `employees` tables.
You must use a SQL inner join to return the records you need based on a connecting column. In the scenario, both tables include the `device_id` column, which you’ll use to perform the join.

1. Run the following query to retrieve all records from the machines table:
SELECT * 
FROM machines;

You’ll note that this query is not sufficient to perform the join and retrieve the information you need.

2. Complete the query to perform an inner join between the machines and employees tables on the device_id column. Replace X and Y with this column name:
SELECT * 
FROM machines 
INNER JOIN employees ON machines.device_id = employees.device_id;

How many rows did the inner join return?
<img width="877" height="258" alt="image" src="https://github.com/user-attachments/assets/b72451e2-7537-4ba9-9d18-1ab7e019b658" />
<img width="874" height="74" alt="image" src="https://github.com/user-attachments/assets/05b8fb8c-eec6-45b3-996e-1ca399114dda" />

## Task 2. Return more data
You now must return the information on all machines and the employees who have machines. Next, you must do the reverse and retrieve the information of all employees and any machines that are assigned to them.

To achieve this, you’ll complete a left join and a right join on the  `employees ` and  `machines ` tables. The results will include all records from one or the other table. You must link these tables using the common  `device_id ` column.

1. Run the following SQL query to connect the `machines` and `employees` tables through a left join. You must replace the keyword `X` in the query:
SELECT * 
FROM machines 
LEFT JOIN employees ON machines.device_id = employees.device_id;

What is the value in the username column for the last record returned?
<img width="891" height="135" alt="image" src="https://github.com/user-attachments/assets/3ff363e8-0c6f-41c6-9106-7be3a9747114" />

2. Run the following SQL query to connect the `machines` and `employees` tables through a right join. You must replace the keyword `X` in the query to solve the problem:
SELECT * 
FROM machines 
RIGHT JOIN employees ON machines.device_id = employees.device_id;

What is the value in the username column for the last record returned?
<img width="889" height="198" alt="image" src="https://github.com/user-attachments/assets/f3dd09de-c575-4d5b-b80e-23a5c0a57e24" />

## Task 3. Retrieve login attempt data
To continue investigating the security incident, you must retrieve the information on all employees who have made login attempts. To achieve this, you’ll perform an inner join on the `employees` and `log_in_attempts` tables, linking them on the common `username` column.

- Run the following SQL query to perform an inner join on the `employees` and `log_in_attempts` tables. Replace X with the name of the right table. Then replace `Y` and `Z` with the name of the column that connects the two tables:
SELECT * 
FROM employees 
INNER JOIN log_in_attempts ON employees.username = log_in_attempts.username;

How many records are returned by this inner join?
<img width="873" height="118" alt="image" src="https://github.com/user-attachments/assets/cd9b1524-2b83-4bd7-a780-39602af1fe72" />




















