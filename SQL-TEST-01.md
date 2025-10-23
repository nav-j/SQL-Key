# Step 1 : Create Table
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("""CREATE TABLE `students`(
                        StudentID int(50),
                        Name Varchar(100),
                        Age int(50),
                        Course Varchar(100),
                        Marks int(50),
                        City Varchar(100)) """)

              
print("Table Created")

cursor.close()
conn.close()
```
- Output :
Table Created
# Step 2 : Insert Sample Data
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("""INSERT INTO `students`() VALUES (1,'Ravi',21,'Computer Science',85,'Delhi'),
                                                  (2,'Neha',20,'Mathematics',78,'Mumbai'),
                                                  (3,'Amit',22,'Computer Science',90,'Pune'),
                                                  (4,'Kavita',19,'Physics',65,'Delhi'),
                                                  (5,'Suresh',21,'Mathematics',88,'Chennai'),
                                                  (6,'Pooja',23,'Computer Science',75,'Bangalore'),
                                                  (7,'Rohan',22,'Physics',58,'Kolkata'),
                                                  (8,'Simran',20,'Mathematics',92,'Delhi')""")

conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
# Step 3 : 
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT * FROM students")



for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(1, 'Ravi', 21, 'Computer Science', 85, 'Delhi')
(2, 'Neha', 20, 'Mathematics', 78, 'Mumbai')
(3, 'Amit', 22, 'Computer Science', 90, 'Pune')
(4, 'Kavita', 19, 'Physics', 65, 'Delhi')
(5, 'Suresh', 21, 'Mathematics', 88, 'Chennai')
(6, 'Pooja', 23, 'Computer Science', 75, 'Bangalore')
(7, 'Rohan', 22, 'Physics', 58, 'Kolkata')
(8, 'Simran', 20, 'Mathematics', 92, 'Delhi')
```
# Step 4 : Tasks
# Task 1 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT * FROM students WHERE Course = 'Computer Science'")



for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(1, 'Ravi', 21, 'Computer Science', 85, 'Delhi')
(3, 'Amit', 22, 'Computer Science', 90, 'Pune')
(6, 'Pooja', 23, 'Computer Science', 75, 'Bangalore')
```
# Task 2 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT Name, Course, Marks FROM students where marks > 80")



for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Ravi', 'Computer Science', 85)
('Amit', 'Computer Science', 90)
('Suresh', 'Mathematics', 88)
('Simran', 'Mathematics', 92)
```
# Task 3 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT Course, AVG(Marks) FROM students GROUP BY Course")



for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Computer Science', Decimal('83.3333'))
('Mathematics', Decimal('86.0000'))
('Physics', Decimal('61.5000'))
```
# Task 4 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT Name, Course, City FROM students where City= 'Delhi'")



for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Ravi', 'Computer Science', 'Delhi')
('Kavita', 'Physics', 'Delhi')
('Simran', 'Mathematics', 'Delhi')
```
# Task 5 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT Name, Marks FROM students WHERE Marks=(SELECT MAX(Marks) from students)")



for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Simran', 92)
```
