# SQL - Basic Record Reading and Sorting 

## Introduction

### Structured Query Language (SQL) is a programming language used to manage and manipulate relational databases. It allows users to query, update, and delete data records. SQL can be used to create and manage database structures like tables and set access permissions. It is essential for applications that require efficient storage, retrieval, and management of data, such as online stores or any data-driven platforms.   
### SQL is important to cybersecurity because it helps protect databases from vulnerabilities and unauthorized access. Many cyberattacks, such as SQL Injection, target database systems to steal or manipulate sensitive information. By understanding SQL, cybersecurity professionals can identify and defend against database-specific threats. They can also monitor database activities and manage permissions.  
---
#### In this screnario, we will work within an organzational database to manage and monitor login activity.   

***Step 1***  
*Your team is investigating failed login attempts that were made after business hours. You want to retrieve this information from the login activity. You’ll identify all unsuccessful attempts after 18:00.*  

The *login_time* column in the *log_in_attempts* table contains information on when login attempts were made. Office hours end at *'18:00'*. 
The *success* column in the *log_in_attempts* table contains values of TRUE or FALSE to indicate whether the login was successful. MySQL stores Boolean values as 1 for TRUE, and 0 for FALSE. This means that TRUE is represented as 1, and FALSE represented as 0 in the *success* column.  

Use the AND operator to retrieve the failed login attempts that occurred after business hours. Replace the X and Y with the correct values to filter for the records you need:  

![get=content](https://github.com/GSecAwareness/SQL/blob/main/1.PNG)  

We create a statement that returns the failed login attempts after 6:00 PM. The FALSE condition represents failed attempts. In this scenario, there were 19 failed attempts after 6:00 PM.  

***Step 2***  
*Your team is investigating a suspicious event that occurred on '2022-05-09'. You want to retrieve all login attempts that occurred on this day and the day before ('2022-05-08').*  

The *login_date* column in the *log_in_attempts* table contains information on the dates when login attempts were made.

Use the OR operator to retrieve the failed login attempts on the specified days. Replace the X and Y with the correct values to filter for the records you need  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/2%20login%20dates.PNG)  

In this condition, we defined two dates, specifically *5-8-2022* and *5-9-2022*. Our output should reflect all login attempts on these two dates, resulting in 75 rows. In both conditions, we must specify *“login_date = “date”*.  

***Step 3***  
*Now, your team is investigating logins that did not originate in Mexico, and you need to find this information. Note that the country field includes entries with 'MEX' and 'MEXICO'. You should use the NOT and LIKE operators and the matching pattern 'MEX%'.*  

Run the following SQL query to retrieve login attempts that did not originate in Mexico. Replace X with the correct operator and Y with the correct pattern to filter for the information you need  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/3%20mexico.PNG)  

This statement returns all values that do not originate from Mexico.  I initially messed this up by not putting NOT in the correct place, resulting in a syntax error. The NOT follows WHERE for correct syntax.   

***Step 4***  

*Retrieve the information from the department and office columns in the employees table.*  

You can run the following SQL query if you need to view the columns and values in the *employees* table  

SELECT *   
FROM employees   
WHERE department = 'Marketing' AND office LIKE 'East%';  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/4%20Marketing.PNG)  

In this example, we first sorted the data to include only results from the Marketing department. In the next part of the statement, we sorted the data to include any Marketing department employee from the East-like offices.   

***Step 5***  

*Now, your team needs to perform a different update to the computers of all employees in the Finance or the Sales department, and you need to locate information on these employees.*  

Write a SQL query to retrieve records for employees in the *'Finance'* or the *'Sales'* department    

![get-content](https://github.com/GSecAwareness/SQL/blob/main/5%20Sales%20Finance.PNG)  

***Step 6***  

*Your team needs to make one more update. This update was already made to employee computers in the Information Technology department. The team needs information about employees who are not in that department. You should use the NOT operator to identify these employees.*  

Write a SQL query to retrieve records for employees who are not in the *'Information Technology'* department  

![get=content](https://github.com/GSecAwareness/SQL/blob/main/6%20IT.PNG)  

This command sorts the output to include any department except IT. Once again, be careful of the NOT operator goes after WHERE.   
























