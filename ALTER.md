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
cursor.execute("ALTER TABLE persons ADD DateOfBirth date")

print("COLUMN ADDED")

cursor.close()
conn.close()
```
- Output :
COLUMN ADDED
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
cursor.execute("ALTER TABLE persons CHANGE Address HomeAddress varchar(100)")

print("COLUMN RENAMED")

cursor.close()
conn.close()
```
- Output :
COLUMN RENAMED
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
cursor.execute("ALTER TABLE persons MODIFY COLUMN City varchar(100)")

print("DATATYPE MODIFIED")

cursor.close()
conn.close()
```
- Output :
DATATYPE MODIFIED
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
cursor.execute("ALTER TABLE persons ADD Email varchar(100)")

print("EMAIL ADDED")

cursor.close()
conn.close()
```
- Output :
EMAIL ADDED
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
cursor.execute("ALTER TABLE persons DROP Email")

print("EMAIL DROPPED")

cursor.close()
conn.close()
```
- Output :
EMAIL DROPPED
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
cursor.execute("ALTER TABLE persons DROP DateOfBirth ")

print("COLUMN DROPPED")

cursor.close()
conn.close()
```
- Output :
COLUMN DROPPED
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
cursor.execute("ALTER TABLE persons ADD Age INT(40) DEFAULT 18")
print("AGE ADDED")

cursor.close()
conn.close()
```
- Output :
AGE ADDED
