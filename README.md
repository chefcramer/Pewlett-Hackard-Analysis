# Pewlett-Hackard-Analysis
Module 7 Employee Databases with SQL

## Overview
This analysis is to determine the number of retiring emplyees by title, and identify employees who are eligible to participate in a mentorship program, to train replacements for the upcoming "silver tsunami" of retiring employees.

## Results
### Analysis 1 : Determining the number of retiring employees by their title.
![retiring_emp_code](https://github.com/chefcramer/Pewlett-Hackard-Analysis/blob/main/write%20up%20resources/retiring%20employees.PNG)

- Using the above section of queries, this will gather the individual employees information (their number, first and last name, title, date hired to date retired), and filtered by their birth date being between 1952 and 1955, indicating retirement age.

   ![retiring_emp_table](https://github.com/chefcramer/Pewlett-Hackard-Analysis/blob/main/write%20up%20resources/retiring%20emp%20table.PNG)

- This image shows the first 20 rows of the retiring employees table generated above. As we can see, there are several duplicate entries as employees are promoted.

   ![unique_title_code](https://github.com/chefcramer/Pewlett-Hackard-Analysis/blob/main/write%20up%20resources/retiring%20distinct.PNG)
   
- This image shows the code that will remove the duplicate entries, by using the `DISTINCT ON (emp_no)` query. This finds the first (most up to date) distinct usage of the employees number, and will discard any older entries.

   ![unique_title_table](https://github.com/chefcramer/Pewlett-Hackard-Analysis/blob/main/write%20up%20resources/retiring%20distinct%20table.PNG)
   
- This image shows the first 20 rows of the revised retiring employees table generated above.

   ![retring_numbers](https://github.com/chefcramer/Pewlett-Hackard-Analysis/blob/main/write%20up%20resources/retiring%20numbers.PNG)
   
- This image shows the query that will return the total number, using the `SELECT COUNT()`, of employees retiring, grouped by their title.

   ![retiring_numbers_table](https://github.com/chefcramer/Pewlett-Hackard-Analysis/blob/main/write%20up%20resources/retiring%20numbers%20table.PNG)
   
- This image shows the total number of employees retiring from PH in the near future, grouped by their title. 

### Analysis 2 : Determining the eligibility of potential mentors.
![mentor_code](https://github.com/chefcramer/Pewlett-Hackard-Analysis/blob/main/write%20up%20resources/mentorship.PNG)

-This image shows the code used to determine the elegibility of potential mentors. It uses the same basic query structure of the retiring employees, using `DISTINCT ON()` to gather only their most recent position, `WHERE` with the date being 01-01-9999 (still employeed), and being born in 1965.
-The choice of using the birth year 1965 is signficant in that they are nearing retirement age, are not likely to change careers this close to retirement.

   ![mentor_table](https://github.com/chefcramer/Pewlett-Hackard-Analysis/blob/main/write%20up%20resources/mentor%20table.PNG)

- This image shows the first 20 rows of the table generated above. 
- The use of a mentorship progam has many advantages. The mentor is nearing retirement age, but isnt there yet. More than likely indicating that they have a large amout of experience to pass on to younger employees, to prepare them to take the place of the large number of retiring employees.

## Summary
- There is a VERY large number of employees that are going to be retiring, indeed a "silver tsunami". There are 90,398 total employees retiring, with 57,668 of them being in a senior position, and 2 of them being managers of entire departments.

Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
