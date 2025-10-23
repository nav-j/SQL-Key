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
cursor.execute("INSERT INTO `employees` (`EmpID`,`Name`,`Department`,`Salary`,`City`) Values (7,'Rajesh','Finance',50000,'Hyderabad')")
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
cursor.execute("SELECT * FROM employees")


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
(5, 'Suresh', 'HR', 30000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Pune')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
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
cursor.execute("INSERT INTO `employees` () Values (8,'Kavita','IT',65000,'Chennai')")
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
cursor.execute("SELECT * FROM employees")


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
(5, 'Suresh', 'HR', 30000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Pune')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Chennai')
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
cursor.execute("""INSERT INTO `employees` (`EmpID`,`Name`,`Department`,`Salary`,`City`) Values (9,'Arjun','HR',35000,'Delhi'),
                                                                                               (10,'Simran','Finance',72000,'Mumbai')""")
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
cursor.execute("SELECT * FROM employees")


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
(5, 'Suresh', 'HR', 30000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Pune')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Chennai')
(9, 'Arjun', 'HR', 35000, 'Delhi')
(10, 'Simran', 'Finance', 72000, 'Mumbai')
```
