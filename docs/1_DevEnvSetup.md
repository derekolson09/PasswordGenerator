## The Build Process
Start by creating a folder to host the program in

Example in this project:
 ```python
   mkdir passgenerator
   cd passgenerator
 ```

> **Note:** this will change based on the name of the project you are working on

### Build the virtual env for package management
```batch
python -m venv passgenVenv
```

### Dev Env Launch
Run this command to get into the virtual environment (copy paste the entire thing)

```batch
passgenVenv\Scripts\activate
(venv) $_
```

### Installing a package

In this example we are installing flask using pip, but it will change to whatever package you want to install into your project.

```batch
    pip install flask
```

### Testing the Virtual Environment

To test if the virtual environment is set up correctly open up a new python interpreter by running the code in your terminal

```batch
    python
```

>   **Note:** 
>  
>   You will see something like this:
>   
>   Python 3.6.5 (v3.6.5:f59c0932b4, Mar 28 2018, 16:07:46) [MSC v.1900 32 bit      (Intel)] on win32
>   Type "help", "copyright", "credits" or "license" for more information.
>   
>   \>>>

In your interpreter type in "import \<package name here>" in this example it will be "import flask"
