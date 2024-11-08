# SQL - Basic Record Reading and Sorting: Part 2

## Introduction

### In this excercise, you'll need to get specific information about employees, their machines, and the departments they’re in. Your team needs this data to perform various tasks, such as running updates, posting a privacy notice in certain departments, and sending an alert to an employee with an issue on a machine.  
---
#### You are responsible for finding the required information by querying a database. You’ll add filters to your queries to locate the information more quickly.  

#### Here’s how you’ll do this task: First, you’ll list all organization machines and their operating systems. Second, you’ll list all machines with the operating system OS 2. Third, you’ll list all the employees in the Finance and Sales departments. Fourth, you’ll obtain information about machines.  
  
***Step 1***    

*Run a SQL query to retrieve only the device_id and operating_system columns from the machines table.*  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/part2/1%20slect%20from.PNG)  

From this picture, you can see that I had syntax problems. The first error was planned  to show what happened when the user forgot to put the semi-colon at the end of the query statement. The second error was not planned, but resulted from an additional space between “from” and “machines.” On the third attempt, the query was successful. As part of my troubleshooting on the third attempt, I capitalized SELECT and FROM, but capitalization is unnceccessary in SQL.   

***Step 2***  

*Select all the records from the machines table with a value of 'OS 2' in the operating_system column. Replace the value X with the correct string*  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/part2/2%20OS%202.PNG)  

The OS 2 value must be enclosed between single quotation marks. In the picture, the semi-colon is on line 2 at the left, but it exists to indicate the end of the statement.  

***Step 3***  

*In this task, you need to retrieve a list of all the employees in the Finance and Sales departments to obtain their office numbers. A notice about handling confidential financial information will be posted to these offices.*  

Filter the rows returned from department column in the *employees* table to include only employees from the *'Finance'* department. Replace X with the appropriate column name and Y with the appropriate value to complete the filter  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/part2/3%20finance.PNG)  

To filter the data, SELECT * was used to extract all the records employees, and finally filter the data by the Finance department. This resulted in our output. The asterisk is a wildcard that represents all columns in a table. When used, the databse returns every column from the table, instead of specific columns.   

*Modify the previous query so that it returns employees who are in the 'Sales' department.*  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/part2/4%20sales.PNG)  


***Step 4***  

*Your team recently discovered that there are issues with machines in the South building. In this task, you need to obtain certain employee and computer information.*  
*A machine in 'South-109' has an issue. You need to determine which employee uses that computer so you can send them an alert.*  

Write a query to identify which employee uses the office in 'South-109'. (The data must be returned from the office column in the employees table.)  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/part2/5%20jlansky.PNG)  

As you can see, I used trial and error to get through this one. I was unsure of the employee field, which is the field I used in attempt two. I scrolled up and realized that the proper column would be username. The picture show the correct output.   

*Next, your team has determined that there is an issue with all the machines in the South building. Offices in the organization are named with the building name, a hyphen, and the office number in that building (for example, 'South-109').*  

Modify the query you used in the previous step so that it returns information on all the employees in the 'South' building. Use the LIKE operator with % in this query.  

![get-content](https://github.com/GSecAwareness/SQL/blob/main/part2/6%20south.PNG)  

In this example, I threw the % operator in the South field, first at the end and then at the beginning. With both errors, I realized that I needed to replace the = sign with the word LIKE. Putting the % back at the end with the correct syntax gave me the desired output.   









