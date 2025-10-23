# Task 1 
- Code :
```
import mysql.connector

conn= mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT * FROM employee where Name like 'R%' ")

for row in cursor.fetchall():
    print(row)


cursor.close()
conn.close()
```
- Output :
```
(1, 'Ramesh ', 'HR', 40000, 'Delhi')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
```
# Task 2 :
- Code :
```
import mysql.connector

conn= mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT * FROM employee where Name like '%a' ")

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
(8, 'Kavita', 'IT', 65000, 'Chennai')
```
# Task 3 :
- Code :
```
import mysql.connector

conn= mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT * FROM employee where Name like '%esh%' ")

for row in cursor.fetchall():
    print(row)


cursor.close()
conn.close()
```
- Output :
```
(1, 'Ramesh ', 'HR', 40000, 'Delhi')
(5, 'Suresh ', 'HR', 30000, 'Chennai')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
```
# Task 4 :
- Code :
```
import mysql.connector

conn= mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT * FROM employee where City like 'D%' ")

for row in cursor.fetchall():
    print(row)


cursor.close()
conn.close()
```
- Ouput :
```
(1, 'Ramesh ', 'HR', 40000, 'Delhi')
(4, 'Neha', 'IT', 45000, 'Delhi')
(9, 'Arjun ', 'HR', 35000, 'Delhi')
```
# Task 5 :
- Code :
```
import mysql.connector

conn= mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT * FROM employee where Name like '_____' ")

for row in cursor.fetchall():
    print(row)


cursor.close()
conn.close()
```
- Output :
```
(2, 'Priya', 'IT', 55000, 'Mumbai')
(6, 'Meena', 'IT', 70000, 'Pune')
```
# Task 6 :
- Code :
```
import mysql.connector

conn= mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT * FROM employee where Name not like 'a%' ")

for row in cursor.fetchall():
    print(row)


cursor.close()
conn.close()
```
- Output :
```
(1, 'Ramesh ', 'HR', 40000, 'Delhi')
(2, 'Priya', 'IT', 55000, 'Mumbai')
(4, 'Neha', 'IT', 45000, 'Delhi')
(5, 'Suresh ', 'HR', 30000, 'Chennai')
(6, 'Meena', 'IT', 70000, 'Pune')
(7, 'Rajesh', 'Finance', 50000, 'Hyderabad')
(8, 'Kavita', 'IT', 65000, 'Chennai')
(10, 'Simran', 'Finance', 72000, 'Mumbai')
```
