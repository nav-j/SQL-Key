
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
cursor.execute("SELECT COUNT(*) FROM employee")

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
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()
cursor.execute("SELECT AVG(Salary) FROM employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(Decimal('52200.0000'),)
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
cursor.execute("SELECT MAX(Salary) FROM employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(72000,)
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
cursor.execute("SELECT MIN(Salary) FROM employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(30000,)
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
cursor.execute("SELECT SUM(Salary) FROM employee")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
(Decimal('522000'),)
# Task 6 :
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
cursor.execute("SELECT Department, AVG(Salary) FROM employee GROUP BY Department")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Finance', Decimal('60666.6667'))
('HR', Decimal('35000.0000'))
('IT', Decimal('58750.0000'))
```
# Task 7 :
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
cursor.execute("SELECT Department, COUNT(*) FROM employee GROUP BY Department")

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
# Task 8 :
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
cursor.execute("SELECT City, SUM(Salary) FROM employee GROUP BY City")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Bangalore', Decimal('60000'))
('Chennai', Decimal('95000'))
('Delhi', Decimal('120000'))
('Hyderabad', Decimal('50000'))
('Mumbai', Decimal('127000'))
('Pune', Decimal('70000'))
```
# Task 9 :
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
cursor.execute("SELECT Department, AVG(Salary) FROM employee GROUP BY Department having AVG(Salary) > 50000")

for row in cursor.fetchall():
    print(row)

cursor.close()
conn.close()
```
- Output :
```
('Finance', Decimal('60666.6667'))
('IT', Decimal('58750.0000'))
```
