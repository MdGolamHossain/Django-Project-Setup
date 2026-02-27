1. UV - Install uv : https://docs.astral.sh/uv/
এটি Python package & virtual environment manage করার জন্য একটি ultra-fast tool।

uv = pip + venv + package manager (super fast version)

# uv কী?
uv হলো একটি modern Python tool যা:

✅ virtual environment তৈরি করে
✅ packages install করে
✅ dependencies manage করে
✅ pip এর চেয়ে অনেক দ্রুত

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

👉 Scaffold = project চালানোর জন্য দরকারি basic structure auto তৈরি।
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



