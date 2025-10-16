# CODE :
```
import mysql.connector

conn = mysql.connector.connect(
    host= "localhost",
    user= "root",
    password= "",
    database= "test"
)

cursor= conn.cursor()

cursor.execute("SELECT * from customers")

for rows in cursor.fetchall():
    print(rows)


cursor.close()
conn.close()
```
# OUTPUT :
```
(1, 'John Doe', '123 Main Street', '110001')
(2, 'Jane Smith', '456 Park Avenue', '220002')
(3, 'Alice Johnson', '789 Green Road', '330003')
```
