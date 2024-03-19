# Ex02 Django ORM Web Application
## Date: 
18/3/24
## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram


![image](https://github.com/Wkrish28/ORM/assets/144295230/34c82a7d-f696-4668-b8bd-16f243c9a01e)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

```
models.py

from django.db import models
from django.contrib import admin
class Train(models.Model):
    Train_code=models.CharField(max_length=20,primary_key=True)
    Train_name=models.CharField(max_length=100)
    start_time=models.DateTimeField()
    End_time=models.DateTimeField()
    start_station_code=models.CharField(max_length=20)
    End_station_code=models.CharField(max_length=20)
 
class TrainAdmin(admin.ModelAdmin):
    list_display=('Train_code','Train_name','start_time','End_time','start_station_code','End_station_code')

admin.py


from django.contrib import admin

from .models import Train, TrainAdmin

admin.site.register(Train, TrainAdmin)

```

## OUTPUT

![image](https://github.com/Wkrish28/ORM/assets/144295230/20979dc0-d3fd-4269-ae6a-c27d2e250bfa)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
