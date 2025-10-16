# Task 1 
- Code:
```
import mysql.connector

conn= mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password= "",
    database= 'test'
)

cursor= conn.cursor()
cursor.execute('SELECT * FROM employees where Department= "IT"')

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(2, 'Priya', 'IT', 55000, 'Mumbai')
(4, 'Neha', 'IT', 45000, 'Delhi')
(6, 'Meena', 'IT', 70000, 'Pune')
```
# Task 2 :
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
cursor.execute('SELECT * FROM employees where Salary > "50000"')

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(2, 'Priya', 'IT', 55000, 'Mumbai')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(6, 'Meena', 'IT', 70000, 'Pune')
```
# Task 3 :
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
cursor.execute('SELECT * FROM employees where City= "Delhi"')

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(1, 'Ramesh', 'HR', 40000, 'Delhi')
(4, 'Neha', 'IT', 45000, 'Delhi')
```
# Task 4 :
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
cursor.execute('SELECT * FROM employees where Salary < "35000"')

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(5, 'Suresh', 'HR', 30000, 'Chennai')
```
# Task 5 :
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
cursor.execute('SELECT * FROM employees where NOT City  = "Mumbai"')

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(1, 'Ramesh', 'HR', 40000, 'Delhi')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(4, 'Neha', 'IT', 45000, 'Delhi')
(5, 'Suresh', 'HR', 30000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Pune')
```
# Task 6 :
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
cursor.execute('SELECT * FROM employees where Salary between 40000 and 60000')

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(1, 'Ramesh', 'HR', 40000, 'Delhi')
(2, 'Priya', 'IT', 55000, 'Mumbai')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(4, 'Neha', 'IT', 45000, 'Delhi')
```
