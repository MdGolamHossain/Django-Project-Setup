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









