# #17 Databases and relations between tables


## Inner Join

## Left Join

````     
                SELECT * FROM students 
                LEFT JOIN students_courses ON fk_students = students.students_id 
                LEFT JOIN courses ON fk_courses = courses.courses_id WHERE students_id = 1
````     

