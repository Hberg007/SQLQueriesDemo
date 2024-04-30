<h1>Apply Filters to SQL Queries Demonstration<h1>


<h2>Description</h2>
Investigate after hours logins via SQL to determine which employee had failed login attempts.
<br />
<br />
<h2>Languages and Utilities Used</h2>

- <b>SQL</b> 


<h2>Environments Used </h2>

- <b>Mac OS</b> 

<h2>Exercise Walk-Through:</h2>
In this exercise, my team recently discovered some potential security issues that involve login attempts after hours. 

I used SQL to examine the organizations employees login attempts to determine where the issues originated.
<br />
<br />
<h2>Retrieve After Hours Failed Login Attempts</h2>
A potential security incident was brought to our attention involving after hours (after 18:00) login attempts. 
<br />
I used SQL to search failed login attempts after hours.
<br />
<br />
The following code demonstrates how I used SQL to filter for failed login attempts that occurred after 6pm (18:00)
<br />
<br />
  <p align="center"> <img width="700" alt="image" src="https://github.com/Hberg007/SQLQueriesDemo/assets/168477827/3167c726-13d7-4165-a13e-069c68228c74")>
<br />
<br />
The first part of the screenshot shows my query, and the second part is a portion of the output.

       I first used the SELECT * (select all) query to search the log in attempts table. 
       
       Using the WHERE clause with an AND operator I then filtered my search down to failed log in attempts that occurred 
       
       after 6pm by writing the condition login_time > ’18:00’ followed by success = ‘0’ which filtered for the failed 
       
       login attempts.
<br />
<br />
<h2>Retrieve Login Attempts on Specific Dates</h2>
<br />
A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or the day prior needs to be investigated.
<br />
<br />
The following screenshot demonstrates the SQL query I created to filter for login attempts that occurred on specific dates.
<br />
<br />
  <p align="center">  <img width="700" alt="image" src="https://github.com/Hberg007/SQLQueriesDemo/assets/168477827/41edd3e8-709c-4f99-9c19-9c00c61e35f2"
<br />
<br />   
The first part of the screenshot displays my SQL query designed to show all login attempts that occurred on 2022-05-09 and 2022-05-08. 
<br />
The second part is a portion of the output.

       To begin, I again used the SELECT *  query to search all the log_in_attempts table.

       I then used a WHERE clause with an OR operator to filter down my results to only login attempts occurring on my 
       
       selected days by using the conditions login_date = ‘2022-05-09’ and login_date = ‘2022-05-08’.
<br/>
<br />
<h2> Retrieve Login Attempts Outside of Mexico:</h2>
<br />
<br />
After investigating the organizations data on login attempts, I discovered an issue with the login attempts that 
<br />
occurred outside of Mexico. I then investigated these login attempts.
<br />
<br />
The following screenshot demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico.
<br />
<br />
  <p align="center">  <img width="700" alt="image" src="https://github.com/Hberg007/SQLQueriesDemo/assets/168477827/bf72b236-4f06-4dd8-bcb3-9ef27fd2b4d2">
<br />
<br />       
The first part of the screenshot is my SQL query, and the second part is a portion of the output which shows 
<br />
the login attempts that occurred outside of Mexico.

        Again, by Using the SELECT * (select all) query to search the log_in_attempts table. 
        
        I used the WHERE clause with NOT to filter for countries other than Mexico.   
        
        I then used LIKE with Mex% as the pattern to match because the dataset represents Mexico. 

        The symbol % is used to represent any number of unspecified characters when used with LIKE                                            
<br />
<br />
<h2> Retrieve Employees in Marketing List:</h2>
<br />
<br />
My team wants to update the computers for certain employees in the Marketing department. 
<br />
To do this, I must get information on which employees machines need updating.
<br />
<br />
The following code demonstrates how I created a SQL query to filter for employee machines in the Marketing department that are in the East building only.
<br />
<br />
 <p align="center"> <img width="700" alt="image" src="https://github.com/Hberg007/SQLQueriesDemo/assets/168477827/15025199-7faf-44e6-b90f-36b6173b7f6f">
<br />
<br />
The first part of the screenshot shows my query, and the second part is a portion of the output that outputs 
<br />
only employees in the marketing department located in the East building.

        I first started by selecting all the data from the employees table. 
        
        Then, I used a WHERE clause with AND to filter for employees who work in the Marketing dept. and located in the East building. 
        
        Using LIKE with East% as the pattern to match to locate the employees in the East building. 
        
        The first condition department = ‘Marketing’ filters for employees in the marketing department only and the second 
        
        condition office LIKE ‘East%’ filters for employees located in the East building.
<br />
<br />
<h2> Retrieve Employees in Finance or Sales List:</h2>
<br />
<br />
The machines for the employees in the Finance and Sales departments also need to be updated. 
<br />
Since a different type of security update is needed, I must get information only from these two departments.
<br />
<br />
The following screenshot demonstrates the SQL code query I created to filter for employee machines from the Finance and Sales departments.
<br />
<br />
 <p align="center"> <img width="700" alt="image" src="https://github.com/Hberg007/SQLQueriesDemo/assets/168477827/516e6084-7268-485f-bb03-3f399102cc14">
<br />
<br />
The first part of the screenshot is my query, and the second part is a portion of the output. 
<br />
This query returns all employees in the Finance and Sales departments.

       Using the SELECT * (select all) query, I searched the employees table. 
       
       Then I used a WHERE clause with OR to filter for employees who are in the Finance and Sales departments. 
       
       I used the OR operator instead of the AND operator because I want all employees who are in either department. 
       
       The first condition department = ‘Finance’,which filters from the Finance department. 
       
       The second condition is department = “Sales’, which filters for employees from the Sales department.
<br />
<br />
<h2> Retrieve All Employees not in IT List:</h2>
<br />
<br />
My team needs to make one more security update on employees who are not in the Information Technology department. 
<br />
To make the update, I first need to retrieve information on these employees.
<br />
<br />
The following code demonstrates how I created a SQL query designed to filter for employee machines from employees not in the I.T. dept.
<br />
<br />
 <p align="center"> <img width="700" alt="image" src="https://github.com/Hberg007/SQLQueriesDemo/assets/168477827/e265e95b-3d22-4633-9629-62f4655e5f80">
<br />
<br />
The first part of the screenshot is my query, the second part is a portion of the output. 
<br />
The query returns all employees not in the Information Technology department. 

        I began my query by selecting all data from the employees table. 
        
        Then, I used a WHERE clause with NOT to filter for employees not in this department.
<br />
<br />
<h2> Summary:
<br />
<br />
I applied filters to SQL queries to get specific information on login attempts, and employee machines. 

I used 2 different tables, log_in_attempts and employees. 
  
I used the AND, OR and NOT operators to filter for the specific information needed to complete each task.
  
I also used LIKE and the percentage sign (%) wildcard to filter for patterns.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
