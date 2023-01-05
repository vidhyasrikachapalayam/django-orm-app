# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Clone the repository and launch django admin.

### STEP 2:
Startapp and migrate myapp and create employee database with help of models.py and admin.py

### STEP 3:
Then runserver and enter atleast 10 employee records into the database.

## PROGRAM
```
MODEL CODE:
from django.db import models
from django.contrib import admin

# Create your models here.
class Employee (models.Model):
    EMP_ID=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    ENAME=models.CharField(max_length=100)
    POST=models.CharField(max_length=100)
    SALARY=models.IntegerField()
    AGE=models.IntegerField(null=32)

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('EMP_ID','ENAME','POST','SALARY','AGE')

ADMIN CODE:

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT
### EMPLOYEE DATATBASE
![Emptable](/images/empdata.png)
### Primary key verification
![Emptable](/images/primary.png)

## RESULT
Database created successfully.