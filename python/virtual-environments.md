---
description: >-
  Information I have come across with Virtual Environments, Packages, and
  Environment Variables
---

# Virtual Environments

## Virtual Environments, Packages, and Environment Variables

I have two different ways listed below for creating Virtual Environments. There are many other options but these are my current favorites. I'm currently looking into `pyenv` for my `python` version management and `poetry` for my package management. My current recommendation is to use `venv` over `pipenv`. Please make sure to add your `venv` folder to your `.gitignore` if you plan to use version control.

{% hint style="info" %}
If you are using windows, I personally have run into a lot of issues with Powershell, I would recommend using cmd prompt.
{% endhint %}

## Documentation:

* venv
  * [https://docs.python.org/3/tutorial/venv.html](https://docs.python.org/3/tutorial/venv.html)
  * [https://docs.python.org/3/library/venv.html\#module-venv](https://docs.python.org/3/library/venv.html#module-venv)
* pipenv
  * [https://pipenv.pypa.io/en/latest/](https://pipenv.pypa.io/en/latest/)
* python-dotenv
  * [https://pypi.org/project/python-dotenv/](https://pypi.org/project/python-dotenv/)
* pip
* [https://pip.pypa.io/en/stable/](https://pip.pypa.io/en/stable/)

## Venv:

The following information is for building a virtual environment via Venv.  You can read more about it at the official python documentation listed above.

### **Create Virtual Environment:**

{% hint style="info" %}
Wherever you run this command it will create a venv folder. If you want the folder to be called something different change the second venv.
{% endhint %}

#### Mac

```bash
$ python3 -m venv venv
```

#### Windows

```text
$ python -m venv venv
```

### Activate Virtual Environment:

#### Mac

```text
$ source venv/bin/activate
(venv) $ _
```

#### Windows

```text
$ venv\Scripts\activate
(venv) $ _
```

### Installing Packages:

```text
(venv) $ pip install package-name
```

{% hint style="info" %}
I have sometimes had packages not install correctly because my pip was out of date.  I have grown a habbit of updating pip when creating a new virtual environment.  This isn't required but it has seemed to help.

`python -m pip install --upgrade pip`
{% endhint %}

### Requirements File:

If you ever need to regenerate your environment on another machine, you are going to have trouble remembering what packages you had to install, so the generally accepted practice is to write a `requirements.txt` file in the root folder of your project listing all the dependencies, along with their versions. Producing this list is actually easy:

```text
(venv) $ pip freeze > requirements.txt
```

The `pip freeze` command will dump all the packages that are installed on your virtual environment in the correct format for the `requirements.txt` file. Now, if you need to create the same virtual environment on another machine, instead of installing packages one by one, you can run:

```text
(venv) $ pip install -r requirements.txt
```

## Pipenv:

The following information is for building a virtual environment via Venv.  You can read more about it at the official python documentation.  [https://pipenv.pypa.io/en/latest/](https://pipenv.pypa.io/en/latest/)  
  
My current recommendation is to use the [venv](virtual-environments.md#venv) option listed above or a mixture of the two. When using `pipenv` the environment folder isn't created inside your project directory. Be mindful you can setup `venv` first and then `pipenv` will use that `venv` location for the environment. Also when using `pipenv` you will get a `pipfile` and `pipfile.lock` for your package dependencies management, so there is no need to create a `requirements.txt` file.  Refer to the [pipenv documentation](https://pipenv.pypa.io/en/latest/) for a detailed description on the two files.

### **Create Virtual Environment:**

Skip this step if you plan to use `venv` for your environment and use `pipenv` for installing packages.

```text
$ pipenv --three
```

### Activate Virtual Environment:

Skip this step if you plan to use `venv` for your environment and use `pipenv` for installing packages.

```text
$ pipenv shell
```

### Installing Packages:

```text
(venv) $ pipenv install package_name
```

## Environment Variables:

Sometimes you need to create environment variables for your project. You can easily create them for your current terminal session with a simple `EXPORT` or `SET` command. The downfall is the variable isn't remembered across terminal sessions. A more popular way is using a package called [python-dotenv](https://pypi.org/project/python-dotenv/), which gives you the ability to store these variables inside a file. If you plan on using version control with the `python-dotenv` method, please remember to hide your environment file in a `.gitignore` file

{% hint style="info" %}
Be mindful you can set variables globally or specific to your virtual environment. Make sure you're inside your virtual environment before running the `export` commands.

When you host applications on [heroku](https://www.heroku.com/) your environment variables are called config variables. Luckily the methods for accessing your environment variables are the same.

If any of these commands don't work for you please visit [https://ss64.com/](https://ss64.com/) for detailed information on your operating system.
{% endhint %}

### EXPORT & SET:

#### MAC

```text
(venv) $ export VAR_NAME=secret
```

#### PC

```text
(venv) $ set VAR_NAME=secret
```

### Python-dotenv:

Create a file in your root directory named `.env`

{% hint style="info" %}
Are you using version control? Add this file to your .gitignore file

It is a common convention to use ALL\_CAPS\_WITH\_SNAKE\_CASE\_FOR\_VARIABLE\_NAMES. There is also no need for spaces before and after the = sign along with no need for quotes for strings.
{% endhint %}

#### Env file example

```text
SECRET_PASSWORD=password123
API_KEY=1234
DATABASE_URI=postgresql://user:password@postgresserver/db
```

### Accessing Environment Variables:

#### EXPORT & SET

```python
import os
print(os.getenv('VAR_NAME'))
print(os.environ.get('VAR_NAME'))
print(os.environ['VAR_NAME'])
```

#### Python-dotenv

{% hint style="info" %}
If you're using flask v1.0 or above you don't need to import and call the load\_dotenv.
{% endhint %}

```python
import os
from dotenv import load_dotenv
load_dotenv()

print(os.getenv('VAR_NAME'))
print(os.environ.get('VAR_NAME'))
print(os.environ['VAR_NAME'])
```

### List Available Variables:

#### MAC

```python
(venv) $ printenv
```

#### PC

```python
(venv) $ SET
```

### Unsetting an EXPORT or SET Variable:

#### MAC

```python
(venv) $ unset VAR_NAME
```

#### PC

```python
(venv) $ SET VAR_NAME=
```

