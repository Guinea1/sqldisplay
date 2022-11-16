# sqldisplay

## A simple package to make displaying MySQL queries much easier

### How do I use it?
Pretty simple, just install with pip(3):
`pip3 install sqldisplay`

And then use it! (example)
```
import mysql.connector
import sqldisplay

db = mysql.connector.connect(
    host="mysql-container",
    user="root",
    passwd="root",
    database="project2"
)

cursor = db.cursor()

query = "SELECT * FROM EmployeesPerRegion WHERE region_name = 'Americas';"
cursor.execute(query)
result = cursor.fetchall()
sqldisplay.format(cursor.description, result)
```
