1. UV - Install uv : https://docs.astral.sh/uv/
এটি Python package & virtual environment manage করার জন্য একটি ultra-fast tool।

uv = pip + venv + package manager (super fast version)

# uv কী?
uv হলো একটি modern Python tool যা:

1. virtual environment তৈরি কর
2. packages install কর
3. dependencies manage কর
4. pip এর চেয়ে অনেক দ্রুতে


## Windows এ uv ইনস্টল 
PowerShell খুলে লিখো:
```
pip install uv
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

```

## Install Check
```
uv --version

```

## uv দিয়ে virtual environment তৈরি

```
uv venv
```

## activate:
```
.venv\Scripts\activate
```

## Django install

```
uv pip install django
```

## uv vs pip + venv 
```
using pip

python -m venv env
env\Scripts\activate
pip install django

using uv

uv venv
uv pip install django
```



# Django Project Setup

using uv: Virtual environment is ready
```
uv init
```
If you run python
```
uv run python -V
```

## Install Django
```
uv add django
```
## Scaffold
এখন Django project তৈরি করলে প্রয়োজনীয় সব file & structure automatic তৈরি হয়ে যায় — এটাকেই scaffold বলা হয়।

-> Scaffold = project চালানোর জন্য দরকারি basic structure auto তৈরি।
Note: single dot (.) mane je directorty ache seta and doulbe dot (..) mane parent directory

## Django project scaffold তৈরি:

```
uv run django-admin startproject config .
```

## Run Project
with django built-in server
```
uv run python manage.py runserver
```

## For Production 
```
uv run python manage.py uvicorn
```

# Django Admin
uv run python manage.py migrate কী?

-> এটি database setup করার command।

🔹 migrate কী করে?

Django default কিছু table তৈরি করে:

1. users
2. admin
3. permissions
4. sessions


-> এই table গুলো database এ তৈরি হয়।

```
uv run python manage.py migrate
```
## Django Admin কী?

-> Django Admin = ready-made dashboard
যেখান থেকে তুমি database manage করতে পারো।

📌 এটি Django এর সবচেয়ে powerful feature।

🔹 Admin দিয়ে কী করা যায়?

1. user add/delete
2. data manage
3. content control
4. permissions manage
5. app data edit
 
-> coding ছাড়াই database control 

## Admin ব্যবহার করতে যা করতে হবে
migrate run
```
uv run python manage.py migrate
```

# superuser তৈরি 

username
email
password

```
uv run python manage.py createsuperuser
```


## Djongo run server 
```
uv run python manage.py runserver
```


## admin panel open

http://127.0.0.1:8000/admin



# Suing Pip

Create virtual environment

```
python -m venv .venv

```
## Activate 
```
.venv\Scripts\activate
```

## Django setup

install django

```
pip install django

```

# Create requirements.txt
create requirements.tex in project folder then wright this command. requirement.txt file a sob library niye asbe

```
pip freeze > .\requirements.txt
```

## Django project create

config ta root app 

```
django-admin startproject config .
```

## Create book app

```
python manage.py startapp book

```

je kono app bananor pore amader akta file create korte hoy urls.py example book app er modde vanate hobe urls.py


# project run


1st

```
python .\manage.py makemigrations

```

2nd

```
python .\manage.py migrate
```

3rd

```
python .\manage.py runserver

```



# Create First Django Project 
1. Make a new project folder

```
makdir main_project
cd main_project
```

2. Create a virtual environment inside the project folder

```
python -m venv venv
python3 -m venv venv ( if python -m venv venv not working )

```

3. Activate the virtual environment
 ```

Windows: venv\Scripts\activate
Linux/macOS: source venv/bin/activate

```


4. install Django inside project folder ( efter activate virtual environment )

```
pip install django
pip3 install django
```

5. Create Start the Django Project

```
Django-admin startproject config .

```

6. Run Your Project


```
python manage.py runserver

```



# Create First App
 1. inside the project directory, use the startapp command to add apps
```
python manage.py startapp myapp

```

# Default Model - migration database table

# run migration command
```
python manage.py migrate

```

#Create new table ( in Models.py )
```
class Book(models.Model):
    id = models.AutoField(primary_key=True)
    text = models.CharField(max_length=100)
    lastName= models.CharField(max_length=50)
```

# Then Migratoins 
```
python manage.py makemigrations
```

# Apply Migrations
```
python manage.py migrate
```

# Modify Model-Migration-database table
1. Add New Column
2. Change Column Name
3. Change Column Data Type
4. Remove Column
5. Change Model name Table name

# 1. Add new Column
```
class Book(models.Model):
    id = models.AutoField(primary_key=True)
    text = models.CharField(max_length=100)
    lastName= models.CharField(max_length=50)
    des= models.CharField(max_length=300, null=True) # Added new column 



```
for execute write 3 terminal command
```
1. enable virtual environment : venv\Scripts\activate
2. python manage.py makemigrations
3. If need check to plan: python manage.py migrate --plan
4. python manage.py migrate
```




































