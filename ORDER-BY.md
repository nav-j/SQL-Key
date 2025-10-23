
# Task 1 :
- Code :
```
import mysql.connector

conn= mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password= "",
    database= 'test'
)

cursor= conn.cursor()

cursor.execute("SELECT * from employees order by Salary")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(5, 'Suresh', 'HR', 30000, 'Chennai')
(1, 'Ramesh', 'HR', 40000, 'Delhi')
(4, 'Neha', 'IT', 45000, 'Delhi')
(2, 'Priya', 'IT', 55000, 'Mumbai')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(6, 'Meena', 'IT', 70000, 'Pune')
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

cursor.execute("SELECT * from employees order by Salary desc")

for rows in cursor.fetchall():
    print(rows)


cursor.close()
conn.close()
```
- Output :
```
(6, 'Meena', 'IT', 70000, 'Pune')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(2, 'Priya', 'IT', 55000, 'Mumbai')
(4, 'Neha', 'IT', 45000, 'Delhi')
(1, 'Ramesh', 'HR', 40000, 'Delhi')
(5, 'Suresh', 'HR', 30000, 'Chennai')
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

cursor.execute("SELECT * from employees order by Department asc,Salary desc")

for rows in cursor.fetchall():
    print(rows)


cursor.close()
conn.close()
```
- Output :
```
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(1, 'Ramesh', 'HR', 40000, 'Delhi')
(5, 'Suresh', 'HR', 30000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Pune')
(2, 'Priya', 'IT', 55000, 'Mumbai')
(4, 'Neha', 'IT', 45000, 'Delhi')
```
