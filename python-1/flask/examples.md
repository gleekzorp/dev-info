---
description: A few examples on various things you will need to do with Flask.
---

# Examples

## Example Template Repo

Throughout this example page, I base a lot of the examples on the following repo.  Please clone or download the example as a base starting point when I mention the use of that repo.

{% hint style="info" %}
After downloading or cloning the repo you will want to set up your virtual environment and install all the packages via the requirements.txt file.  [Learn more](../virtual-environments.md#virtual-environments-packages-and-environment-variables)
{% endhint %}

## Simple Example From Flask Docs:

If you go to the Flask docs you will see a very simple example to quickly teach you the simple concepts and I have that listed below.  I would recommend taking a look at the [Better Simple Example](examples.md#better-simple-example) afterward.  I got the idea for this better example from [The Flask Mega Tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world).

Create a new file called `app.py`, paste the following code, and then inside your terminal run `python app.py`.

{% hint style="warning" %}
Don't forget to be inside your virtual environment.  [Learn more](../virtual-environments.md)
{% endhint %}

{% hint style="info" %}
Want to know what `__name__` means?  [Learn more](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)
{% endhint %}

```python
from flask import Flask

app = Flask(__name__)


@app.route('/')
def hello_world():
    return 'Hello World!'


if __name__ == "__main__":
    app.run(debug=True)

```

## Better Simple Example:

Coming soon...

