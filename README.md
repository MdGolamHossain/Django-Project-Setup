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
