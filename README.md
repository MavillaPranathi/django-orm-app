# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram



## DESIGN STEPS

### STEP 1:
```
Create a django project using "django-admin startproject studentproject"

   We will get a new folder
   
   Now go into student project folder using "cd studentproject"

   create a new folder inside studentproject using "python3 manage. py startapp stueligibility "

   In settings .py allow host and add the folder "aadhardetails" in installed apps.

   Save the file

   And in terminal : "python3 manage. py runserver 0:80"
   ```

### STEP 2:
```
Open new terminal

   change directory to studentproject "Cd studentproject"

   make migrations using "python3 manage.py makemigrations"

                         "python3 manage.py migrate"

   create a super user "python3 manage.py createsuperuser"

   create username ,email id and password 

   python3 manage.py runserver 0:80

   log in to django administration using username and password
   ```
### STEP 3:
```
Go to aadhardetails - models.py
   
   code the program and save it

   Go to admin .py 

   code and save it

   Now make migrations 
   
   Make sure we are inside studentproject folder and now run the application using "python3 manage.py runserver 0:80"

   Now search the url of the website in chrome,log in and create tables
```
## PROGRAM

### models.py:
```
from django.db import models
from django.contrib import admin
class Student (models.Model):
    aadharnumber= models.IntegerField(primary_key=True)
    name = models.CharField(max_length=50)
    dateofbirth = models.DateField()
    mobilenumber= models.IntegerField()
    address = models.CharField(max_length=20)
class StudentAdmin (admin.ModelAdmin):
    list_display = ('aadharnumber','name','dateofbirth','mobilenumber','address')
```

### admin.py:
```
from django.contrib import admin
from .models import Student,StudentAdmin

admin.site.register(Student,StudentAdmin)
```

## OUTPUT

![Screenshot (30)](https://user-images.githubusercontent.com/118343610/214348395-02637076-9152-4613-bc2a-76dd0fca34e2.png)
![Screenshot (31)](https://user-images.githubusercontent.com/118343610/214348456-6cd0725d-c263-4c96-81bf-86ae7fddada5.png)

![Screenshot (29)](https://user-images.githubusercontent.com/118343610/214348693-29420118-47b7-4fa8-8197-895c304d46a5.png)




## RESULT
Develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).
