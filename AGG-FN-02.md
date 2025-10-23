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
cursor.execute("SELECT Count(*) from employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(10,)
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
cursor.execute("SELECT SUM(Salary) from employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(Decimal('522000'),)
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
cursor.execute("SELECT AVG(Salary) from employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(Decimal('52200.0000'),)
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
cursor.execute("SELECT Department, COUNT(*) from employee GROUP BY Department ")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Finance', 3)
('HR', 3)
('IT', 4)
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
cursor.execute("SELECT Department, SUM(Salary) from employee GROUP BY Department ")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Finance', Decimal('182000'))
('HR', Decimal('105000'))
('IT', Decimal('235000'))
```
# Task 6 :
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
cursor.execute("SELECT City ,AVG(Salary) from employee GROUP BY City ")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Bangalore', Decimal('60000.0000'))
('Chennai', Decimal('47500.0000'))
('Delhi', Decimal('40000.0000'))
('Hyderabad', Decimal('50000.0000'))
('Mumbai', Decimal('63500.0000'))
('Pune', Decimal('70000.0000'))
``` 
