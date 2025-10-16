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
cursor.execute("UPDATE employees set Salary = 45000 where EmpID = 1")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Code To see Output :
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
(1, 'Ramesh', 'HR', 45000, 'Delhi')
(2, 'Priya', 'IT', 55000, 'Noida')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(4, 'Neha', 'IT', 45000, 'Noida')
(5, 'Suresh', 'HR', 30000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Noida')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Noida')
(9, 'Arjun', 'HR', 35000, 'Delhi')
(10, 'Simran', 'Finance', 72000, 'Mumbai')
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
cursor.execute("UPDATE employees set City = 'Noida' where Department = 'IT'")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Code to see Output :
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
(1, 'Ramesh', 'HR', 45000, 'Delhi')
(2, 'Priya', 'IT', 55000, 'Noida')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(4, 'Neha', 'IT', 45000, 'Noida')
(5, 'Suresh', 'HR', 30000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Noida')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Noida')
(9, 'Arjun', 'HR', 35000, 'Delhi')
(10, 'Simran', 'Finance', 72000, 'Mumbai')
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
cursor.execute("UPDATE employees set Salary = Salary+5000 where Department = 'HR'")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Code to see Output :
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
(5, 'Suresh', 'HR', 35000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Noida')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Noida')
(9, 'Arjun', 'HR', 40000, 'Delhi')
(10, 'Simran', 'Finance', 72000, 'Mumbai')
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
cursor.execute("UPDATE employees set Department = 'IT' where EmpID = 10")
conn.commit()

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Code to see Output :
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
(5, 'Suresh', 'HR', 35000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Noida')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Noida')
(9, 'Arjun', 'HR', 40000, 'Delhi')
(10, 'Simran', 'IT', 72000, 'Mumbai')
```
