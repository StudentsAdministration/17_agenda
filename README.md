# #17 Databases and relations between tables


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

