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
cursor.execute("SELECT * FROM employee limit 3")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()          
```
- Output :
```
(1, 'Ramesh ', 'HR', 40000, 'Delhi')
(2, 'Priya', 'IT', 55000, 'Mumbai')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
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
cursor.execute("SELECT * FROM employee ORDER BY Salary DESC limit 5")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(10, 'Simran', 'Finance', 72000, 'Mumbai')
(6, 'Meena', 'IT', 70000, 'Pune')
(8, 'Kavita', 'IT', 65000, 'Chennai')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
(2, 'Priya', 'IT', 55000, 'Mumbai')
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
cursor.execute("SELECT * FROM employee WHERE NOT EmpID= 1 LIMIT 2")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()          
```
- Output :
```
(2, 'Priya', 'IT', 55000, 'Mumbai')
(3, 'Anil', 'Finance', 60000, 'Bangalore')
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
cursor.execute("SELECT * FROM employee WHERE Department = 'IT' limit 2")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()          
 ```
- Output :
```
(2, 'Priya', 'IT', 55000, 'Mumbai')
(4, 'Neha', 'IT', 45000, 'Delhi')
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
cursor.execute("SELECT * FROM employee ORDER BY Salary ASC limit 3")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()          
```
- Output :
```
(5, 'Suresh ', 'HR', 30000, 'Chennai')
(9, 'Arjun ', 'HR', 35000, 'Delhi')
(1, 'Ramesh ', 'HR', 40000, 'Delhi')
```
