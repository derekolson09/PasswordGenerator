### Initializing the application
Initialize an app folder by using this command in the terminal while still inside the project directory, in this case the passgenerator directory.

```batch
    mkdir app
```

Then inside your app folder create a new file called \_\_init__.py

Inside your file called \_\_init__.py insert the following code:

```python
from flask import Flask
app = Flask(__name__)

from app import routes
```

> **The code explained:**
>
>   This script creates an instance of the Flask object which is imported from the flask package
> Then the name (the name of the module) variable is passed to the Flask class. The location of the module is then used to be the starting point of the application. Then the routes module is imported from the app variable which is the flask object. Inside this module import will be the different url paths available to the application.
>
> **IMPORTANT**
>
> The order with which the code is presented above must be the order in the actual python script since it prevents circular imports by using the import at the bottom.

Inside the app folder create a new script file called routes.py

Next, inside the routes.py file insert the following code:

```python
from app import app

@app.route('/')
@app.route('/index')
def index():
    return "Hello World!"
```

Using the @app decorator allows a modification to the function below it. Therefore, once this application is launched then the index function will be called from either the / or /index url pattern which simply returns a hello world string.

Now, go to the root directory of the application (passgenerator) and create a new file called passgen.py.
In this file, insert the following code:
```python
from app import app
```

The next step is to create a new file called .flaskenv inside the root application directory, in this case passgenerator.
Inside the .flaskenv file you will insert

Next, in our virtual environment we will import a new package called python-dotenv.

In your virtual environment install the package by using the following command.
```
pip install python-dotenv
```
This is used to allow us to set the environment for the application without constantly having to type export FLASK_APP=passgen.py in each new instance of your terminal.