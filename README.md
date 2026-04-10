📌 Django CRUD Application

This is a simple CRUD (Create, Read, Update, Delete) web application built using the Django framework. It allows users to add, view, update, and delete records.

🚀 Features

Add new user data

View all records

Update existing records

Delete records

Django admin panel support

Success messages for actions

🛠️ Technologies Used

Python

Django

HTML

CSS (Bootstrap form styling)

📂 Project Structure
```
my_site/
│
├── myapp/
│   ├── admin.py
│   ├── models.py
│   ├── forms.py
│   ├── views.py
│
├── my_site/
│   ├── urls.py
│
├── templates/
│   ├── index.html
│   ├── update.html
│
└── manage.py
```
📊 Model

The project uses a single model:
```
class Data(models.Model):
    name = models.CharField(max_length=30)
    contact = models.CharField(max_length=30)
    address = models.CharField(max_length=30)
    mail = models.CharField(max_length=30)

    class Meta:
        db_table = "data"
```
🧾 Form

A Django ModelForm is used for handling user input:
```
class RegisterForm(forms.ModelForm):
    class Meta:
        model = Data
        fields = ['name','contact','address','mail']
```
🌐 URL Routes

URL	Function
```
/	Home page (View & Add data)
/addData	Add new record
/updateData/<id>	Update record
/deleteData/<id>	Delete record
/admin/	Django admin panel
```
⚙️ How to Run the Project

Clone the repository

git clone https://github.com/haripriyan300-cpu/Django_CRUD_Application.git

Navigate to project folder

cd my_site

Install dependencies

pip install django

Apply migrations

python manage.py makemigrations

python manage.py migrate

Run the server

python manage.py runserver

Open in browser

http://127.0.0.1:8000/

🔑 Admin Panel

To access admin panel:

Create superuser

python manage.py createsuperuser

Open

http://127.0.0.1:8000/admin/

📌 Functional Overview

Home Page → Displays all records and form to add data

Add Data → Saves new record to database

Update Data → Edits existing record

Delete Data → Removes record from database

