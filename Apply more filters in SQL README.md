# Apply more filters in SQL

## Scenario
In this scenario, you’re investigating a recent security incident.

You need to gather information about login attempts for certain dates and times. This will help in resolving a security incident.

Here’s how you’ll do this task: `First`, you’ll retrieve login events made after a certain date. `Second`, you’ll narrow the focus of the search to filter logins in a date range. `Third`, you’ll investigate logins that were made at certain times. `Finally`, you’ll filter login attempts based on their event IDs.

It's time to get started and use operators to filter data from a table!

-----
## Task 1. Retrieve login attempts after a certain date
In this task, you need to investigate a recent security incident. To do this, you need to gather information about login attempts made after a certain date.

1. Complete the SQL query to retrieve data for login attempts made after `'2022-05-09'`. Replace X with the correct operator:
SELECT * 
FROM log_in_attempts 
WHERE login_date > '2022-05-09';

How many login attempts were made after 2022-05-09?
<img width="778" height="230" alt="Screenshot 2025-11-13 002647" src="https://github.com/user-attachments/assets/215848f7-15f6-418a-b71f-4290bb35d6a0" />
<img width="777" height="67" alt="image" src="https://github.com/user-attachments/assets/979e85bd-18f6-4873-94ae-034293708a1d" />

`Now`, based on your first query, you find a need to expand the date range to include 2022-05-09 in your search.

2.Complete the SQL query to retrieve data for login attempts that were made on or after `'2022-05-09'`. Replace `X` with the correct operator:
SELECT * 
FROM log_in_attempts 
WHERE login_date >= '2022-05-09';

How many login attempts were made on or after 2022-05-09?
<img width="777" height="218" alt="image" src="https://github.com/user-attachments/assets/7bf77fd2-2646-4d93-a71c-6a57dc67bb6c" />
<img width="779" height="96" alt="image" src="https://github.com/user-attachments/assets/392675da-590d-4831-afd9-3ac074a04ff5" />


## Task 2. Retrieve logins in a date range
In this task, you need to narrow the focus of the search. Login attempts made after 2022-05-11 shouldn't be included. Use the  `BETWEEN ` and  `AND ` operators to return results between  `'2022-05-09' ` and  `'2022-05-11' `.
SELECT * 
FROM log_in_attempts 
WHERE login_date BETWEEN '2022-05-09' AND '2022-05-11';

How many login attempts were made between 2022-05-09 and 2022-05-11?
<img width="778" height="284" alt="image" src="https://github.com/user-attachments/assets/88b8502e-d434-4f7b-a9b1-c3d839033876" />
<img width="775" height="98" alt="image" src="https://github.com/user-attachments/assets/c20b7bb0-bb8e-4db5-84b1-76bf1844f12b" />

## Task 3. Investigate logins at certain times
In this task, you need to investigate logins that were made at certain times. To do this, filter the data in the `log_in_attempts`table by login time (`login_time`).

`First`, your organization's typical work hours begin at 07:00:00. Retrieve all login attempts made before 07:00:00 to learn more about the users who are logging in outside of typical hours.

1. Write a SQL query to retrieve data for login attempts made before `'07:00:00'`.
<img width="777" height="373" alt="image" src="https://github.com/user-attachments/assets/b4e3cb65-cd23-4b94-b0bc-635983d0e44a" />

The query in the previous step returned more results than required.

2. Modify the query to return logins between `'06:00:00'` and `'07:00:00'`.
What time was the earliest login attempt between 06:00:00 and 07:00:00?

<img width="781" height="458" alt="image" src="https://github.com/user-attachments/assets/09b06290-72e3-44ed-a14b-c2f0457cf8ad" />

## Task 4. Investigate logins by event ID
In this task, you need to investigate login attempts based on event ID numbers. With this query, you want to return only the `event_id`, `username`, and `login_date` fields from the `log_in_attempts` table.

1. Write a query to return login attempts with event_id greater than or equal to `100`.

<img width="555" height="289" alt="image" src="https://github.com/user-attachments/assets/cf3fc969-59de-4caa-8948-6ba19bc04439" />

The query in the previous step returned more data than required.

2. Modify the query to return only login attempts with event_id between `100` and `150`.
<img width="560" height="378" alt="image" src="https://github.com/user-attachments/assets/c0a844d4-70ed-43c5-b86c-c52ba82fa8f4" />

