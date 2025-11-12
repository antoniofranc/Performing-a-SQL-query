# SQL Basic Queries Lab

## Scenario
In this scenario, you have to determine which employee devices must be updated. You also need to investigate user login activity to explore if any unusual activity has occurred.

The information you need is located in the `machines` and `login_attempts` tables in the `organization` database.

Here’s how you’ll do this task: `First`, you’ll obtain information on the employee devices that must be updated. `Next`, you’ll examine the login attempts for unusual activity. `Finally`, you’ll use the ORDER BY keyword to sort the data returned by your SQL queries.

-----
## Task 1. Retrieve employee device data
In this task, you need to obtain information on employee devices because your team needs to update them. The information you need is in the `machines` table in the `organization` database.
Run the following query to select all device information from the machines table:

SELECT *
FROM machines;

`Note`: Using the asterisk (*) returns all data from the specified table. Also, table names in MySQL are case-sensitive.
<img width="574" height="294" alt="image" src="https://github.com/user-attachments/assets/b0237231-a798-4238-8523-81754cb3f07a" />
<img width="134" height="298" alt="image" src="https://github.com/user-attachments/assets/86486b68-365d-49e2-bb36-4beaebb97bed" />
`Next`, you want to focus on the email client running on various devices.

2. Run the following query to select only the device_id and email_client columns from the machines table :
What email client is returned in the third row?
<img width="672" height="334" alt="Screenshot 2025-11-12 142950" src="https://github.com/user-attachments/assets/66a36f7f-5677-45e6-a8ed-aeeba6195297" />

`Now`, you need information on the operating systems used on various devices and their last patch date.

3. Complete the query to return only the `device_id`, `operating_system`, and `OS_patch_date` columns from the `machines` table:
What is the patch date of the first entry?
<img width="784" height="163" alt="Screenshot 2025-11-12 143220" src="https://github.com/user-attachments/assets/9da8f2d3-6c7e-42c6-83db-d8531e26d4db" />

-----

## Task 2. Investigate login activity
In this task, you need to analyze the information from the `log_in_attempts` table to determine if any unusual activity has occurred.

`First`, you need to investigate the locations where login attempts were made to ensure that they’re in expected areas (the United States, Canada, or Mexico).

1. Write a SQL query to select the `event_id` and `country` columns from the `log_in_attempts` table.
<img width="805" height="453" alt="Screenshot 2025-11-12 144414" src="https://github.com/user-attachments/assets/efdafe49-f1de-42cc-a1d8-06b30738cd34" />

2. Write a SQL query that selects the `username`, `login_date`, and `login_time` columns from the `log_in_attempts` table.
What username is returned in the fifth row?
<img width="775" height="361" alt="Screenshot 2025-11-12 144544" src="https://github.com/user-attachments/assets/05e09480-455d-4549-959f-0677cb996c6b" />

`Now`, you need to get a complete picture of all login attempts.

3.Write a SQL query that selects all columns from the `log_in_attempts` table, using a single symbol after the `SELECT` keyword.
<img width="782" height="223" alt="Screenshot 2025-11-12 144647" src="https://github.com/user-attachments/assets/e0cae77f-7386-4281-987c-d311ee27743a" />

---

## Task 3. Order login attempts data
In this task, you need to use the `ORDER BY` keyword. You'll sequence the data that your query returns according to the login date and time.

`First`, you need to sort the information by date.

1. Run the following query, which orders `log_in_attempts` data by `login_date`:
SELECT *
FROM log_in_attempts
ORDER BY login_date;

What are the username and login date of the first record returned?
<img width="782" height="223" alt="Screenshot 2025-11-12 144647" src="https://github.com/user-attachments/assets/a8c58f1b-a3fd-4b52-86be-0c1ec68c86b6" />






















