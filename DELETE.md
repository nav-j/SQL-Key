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
cursor.execute("DELETE FROM employees where EmpID = 5")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Code to see Output :                      (# Same code is used to see output in every task after Deletion)
```
import mysql.connector

conn= mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password= "",
    database= 'test'
)

cursor= conn.cursor()
cursor.execute("SELECT * from employees")


for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(1, 'Ramesh', 'HR', 50000, 'Delhi')
(2, 'Priya', 'IT', 55000, 'Noida')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(4, 'Neha', 'IT', 45000, 'Noida')
(6, 'Meena', 'IT', 70000, 'Noida')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Noida')
(9, 'Arjun', 'HR', 40000, 'Delhi')
(10, 'Simran', 'IT', 72000, 'Mumbai')
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
cursor.execute("DELETE FROM employees where Department = 'HR'")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(2, 'Priya', 'IT', 55000, 'Noida')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(4, 'Neha', 'IT', 45000, 'Noida')
(6, 'Meena', 'IT', 70000, 'Noida')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Noida')
(10, 'Simran', 'IT', 72000, 'Mumbai')
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
cursor.execute("DELETE FROM employees where City = 'Delhi'")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(2, 'Priya', 'IT', 55000, 'Noida')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(4, 'Neha', 'IT', 45000, 'Noida')
(6, 'Meena', 'IT', 70000, 'Noida')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Noida')
(10, 'Simran', 'IT', 72000, 'Mumbai')
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
cursor.execute("DELETE FROM employees where Salary <40000")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(2, 'Priya', 'IT', 55000, 'Noida')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(4, 'Neha', 'IT', 45000, 'Noida')
(6, 'Meena', 'IT', 70000, 'Noida')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Noida')
(10, 'Simran', 'IT', 72000, 'Mumbai')
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
cursor.execute("DROP TABLE employees")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
TABLE DELETED
