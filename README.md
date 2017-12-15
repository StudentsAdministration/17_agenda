# #17 Databases and relations between tables

## What we will cover today
Today we will work with raltions between tables.     
So far you have worked with one table (e.g. students). But a student can be in a class for instance this one, SWC 2<sup>nd</sup> Semester. And the class and the student is related. How this is model in a database we will look at today.    

There are 3 types of relations in a ralational database:

* one to one
* **one to many**
* many to many

We will start with the **"One to Many"** relation and look at the 2 others next time.

<div width="300px">![](https://github.com/StudentsAdministration/17_agenda/blob/master/slides/en-mange.png)</div>
![](https://github.com/StudentsAdministration/17_agenda/blob/master/slides/en-mange-tabeller.png)


### Joining the tables in a query
When we have modeled the database (created the tables and made the connections) we also need to query the tables (like we did so fare with the SELECT statement). For this we need to join or merge the table data.

This semester you will learn about 3 types of JOINS:

* **INNER JOIN**
* LEFT JOIN
* RIGHT JOIN

Today we will work with the **INNER JOIN** and look at the 2 others next time.

* [Slides from Today](https://github.com/StudentsAdministration/17_agenda/blob/master/slides/Database_Modeling_Relationships.pdf)

## Inner Join
<sub>[Link to literature](https://www.w3schools.com/sql/sql_join_inner.asp)</sub>    

A INNER JOIN returns records that have matching values in both tables.

![Inner Join](https://www.w3schools.com/sql/img_innerjoin.gif)      

The INNER JOIN keyword selects records that have matching values in both tables.

## Left Join
<sub>[Link to literature](https://www.w3schools.com/sql/sql_join_left.asp)</sub>    

A LEFT JOIN returns all records from the left table, and the matched records from the right table. 

![Inner Join](https://www.w3schools.com/sql/img_leftjoin.gif)    

The LEFT JOIN keyword returns all records from the left table (table1), and the matched records from the right table (table2). The result is NULL from the right side, if there is no match.

An example from the StudentsAdministration application.
````     
                SELECT * FROM students 
                LEFT JOIN students_courses ON fk_students = students.students_id 
                LEFT JOIN courses ON fk_courses = courses.courses_id WHERE students_id = 1
````     
Here we get the student with the id = 1 since there is a left join we are sure to get the student even if the student have no enrollments yet. Then we get the content of the students_courses table if they exits (if the student are enrolled at any courses), and in the last LEFT JOIN we get the info of the course that the student are enrolled at.

If we would have used an INNER JOIN nothing would have been selected if the student did not have any enrollments.

## Right Join
<sub>[Link to literature](https://www.w3schools.com/sql/sql_join_right.asp)</sub>     

The RIGHT JOIN returns all records from the right table, and the matched records from the left table

![Inner Join](https://www.w3schools.com/sql/img_rightjoin.gif) 

The RIGHT JOIN keyword returns all records from the right table (table2), and the matched records from the left table (table1). The result is NULL from the left side, when there is no match.    

## Literature

* [Slides from Today](https://github.com/StudentsAdministration/17_agenda/blob/master/slides/Database_Modeling_Relationships.pdf)
* [SQL Joins](https://www.w3schools.com/sql/sql_join.asp)
* [SQL INNER JOIN](https://www.w3schools.com/sql/sql_join_inner.asp)
* [SQL LEFT JOIN](https://www.w3schools.com/sql/sql_join_left.asp)
* [SQL RIGHT JOIN](https://www.w3schools.com/sql/sql_join_right.asp)

