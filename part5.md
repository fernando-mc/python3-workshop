# A Complete Beginner's Introduction to Python

## Part 5

### Python Libraries

Python libraries are one of the most amazing things about Python. They are bits of code that the developers of the Python programming language decided could be useful to Python developers and included for us with Python!

Go ahead and open up the Python interpreter now in the VS Code terminal with `python3`.

Inside the terminal, type this out:

```python
import math
math.sqrt(16)
```

The first line of this brings in the `math` module to our Python interpreter and allows us to use some of the cool features it offers. The second line, takes advantage of one of these, `sqrt`, short for "square root". Then it takes the square root of 16 and gives us 4.

We can also import other libraries that aren't included in the standard library, but to do that we have to install them first. In a moment, we'll look at how we can use `pip` to do just that, but first we need to learn about `venv`.

### Using venv

Venv stands for **V**irtual **Env**ironment. 

A Python virtual environment is basically a nice clean workshop where you can build something in Python without having to worry about different tools lying around for you to accidentally stub your toe on.

So how do we use venv? Well, we start from the command line. In your VS Code Terminal navigate to the folder for your Python project and type out this command:

`python3 -m venv venv`

Let's break this command down into it's different parts:

- `python3` - We start with `python3` to access the various functionality of Python 3.
- `-m` is a 'flag' that is added to the command to specify the value following it will be a Python "Module" that we can do something with. Modules are files that contain useful bits of Python code that we can use again.
- The first `venv` is the name of the Python 3 module we want to use.
- The second `venv` could also be `penguin` or `flamingo` or anything else we wanted to name our virtual environment.

Go ahead and run the command now, (on some Windows machines it might take a minute so don't worry if it does).

After you see your Terminal prompt indicate it is ready again, list out the contents of the directory with `dir` or `ls`. You should see a new directory called `venv` (or `penguin`/`flamingo` if you decided to be edgy).

That `venv` directory is our new virtual environment! Now, the last thing we need to do before we use it is to activate it. To do that you can run the following commands:

On Mac/Linux you can run `source venv/bin/activate`.

On Windows you can run `venv\Scripts\activate`.

Once those commands are run you should see `(venv)` appear to the left of your Terminal prompt. This means you have created and activated your virtual environment correctly!

Now that the environment is turned on, you're actually using an entirely different installation of Python 3 that lives inside this folder. Also, you can now install Python packages (more on these in just a sec!) in this virtual environment. 

#### What Python am I using?

Try this, type out: `which python3` (Linux/Mac) or `where python3` (Windows). `which` and `where` are commands that let you know what you're working with when you type out a command into the terminal. When you hit enter, you should see a result that includes the `venv` directory you just created.

Now try this, turn off the virtual environment by typing out `deactivate` and pressing enter. You should notice the `(venv)` disappear from your Terminal prompt.

Then run the same `which python3` or `where python3` again. It should give you a different result that doesn't include `venv`. This means the installation of Python it is referencing lives somewhere else on your computer.

So what we did was to create our on little Python workshop to work in!

### Installing Python Packages with pip!

Now that we know how to create and activate virtual environments. Let's see how we can install a Python package inside of ours using Python's package manager tool - `pip`.

First, make sure you turn your `venv` environment back on using either
`source venv/bin/activate` (Max/Linux) or `venv\Scripts\activate` (Windows).

Now, run this command:

`pip freeze`

It probably wont output anything. That's because `pip freeze` is used to show us what we've installed in our environment. Because we haven't installed anything yet it doesn't output anything!

So let's install a package. Use `pip install requests` to install the `requests` package.

This should produce a decent bit of output in our terminal that looks something like this:

```
Collecting requests
  Using cached https://files.pythonhosted.org/packages/51/bd/23c926cd341ea6b7dd0b2a00aba99ae0f828be89d72b2190f27c11d4b7fb/requests-2.22.0-py2.py3-none-any.whl
Collecting certifi>=2017.4.17 (from requests)
  Using cached https://files.pythonhosted.org/packages/60/75/f692a584e85b7eaba0e03827b3d51f45f571c2e793dd731e598828d380aa/certifi-2019.3.9-py2.py3-none-any.whl
Collecting chardet<3.1.0,>=3.0.2 (from requests)
  Using cached https://files.pythonhosted.org/packages/bc/a9/01ffebfb562e4274b6487b4bb1ddec7ca55ec7510b22e4c51f14098443b8/chardet-3.0.4-py2.py3-none-any.whl
Collecting idna<2.9,>=2.5 (from requests)
  Using cached https://files.pythonhosted.org/packages/14/2c/cd551d81dbe15200be1cf41cd03869a46fe7226e7450af7a6545bfc474c9/idna-2.8-py2.py3-none-any.whl
Collecting urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 (from requests)
  Using cached https://files.pythonhosted.org/packages/e6/60/247f23a7121ae632d62811ba7f273d0e58972d75e58a94d329d51550a47d/urllib3-1.25.3-py2.py3-none-any.whl
Installing collected packages: certifi, chardet, idna, urllib3, requests
Successfully installed certifi-2019.3.9 chardet-3.0.4 idna-2.8 requests-2.22.0 urllib3-1.25.3
You are using pip version 19.0.3, however version 19.1.1 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
```

Essentially what this tells us is that `pip` is going out and getting the `requests` package *and any packages that `requests` itself depends on to work*. Now if we run `pip freeze` again we should see something like this:

```
certifi==2019.3.9
chardet==3.0.4
idna==2.8
requests==2.22.0
urllib3==1.25.3
```

This now shows us the installed packages and the versions of each of them. This is a great sign! To confirm the installation went well, we can open up the Python interpreter with `python3` and then type out `import requests` and hit enter.

If the command doesn't throw a Traceback we've succeeded and we're ready to start using `requests` in a fun project in the next section! 

## [Next... Part 6](part6.md)

### [Previous... Part 4](part4.md)