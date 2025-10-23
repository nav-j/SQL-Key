# Task 1 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password= "",
    database= 'test'
)

cursor= conn.cursor()
cursor.execute("SELECT MIN(Salary) from employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(30000,)

# Task 2 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password= "",
    database= 'test'
)

cursor= conn.cursor()
cursor.execute("SELECT MAX(Salary) from employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(72000,)
# Task 3 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password= "",
    database= 'test'
)

cursor= conn.cursor()
cursor.execute("SELECT Department, MIN(Salary),MAX(Salary) from employee GROUP by Department")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output
```
('Finance', 50000, 72000)
('HR', 30000, 40000)
('IT', 45000, 70000)
```
# Task 4 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password= "",
    database= 'test'
)

cursor= conn.cursor()
cursor.execute("SELECT * from employee where Salary=(SELECT max(Salary) from employee)")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(10, 'Simran', 'Finance', 72000, 'Mumbai')
```
# Task 5 :
- Code :
```
import mysql.connector

conn = mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password= "",
    database= 'test'
)

cursor= conn.cursor()
cursor.execute("SELECT * from employee where Salary=(SELECT MIN(Salary) from employee where Department = 'IT')")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
(4, 'Neha', 'IT', 45000, 'Delhi')
```
