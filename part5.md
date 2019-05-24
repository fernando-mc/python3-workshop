# A Complete Beginner's Introduction to Python

## Part 5

### Using Venv

Venv stands for **V**irtual **Env**ironment. 

In this context, a virtual environment is basically a nice clean workshop where you can build something in Python without having to worry about different tools lying around for you to accidentally stub your toe on.

Venv helps us build a Python project by allowing us to install *dependencies* inside of a special folder that is restricted to a particular project. This allows us to avoid conflicts if one piece of code breaks another piece. It also helps us to keep track of what dependencies we're actually using on a given project. 

This also helps us avoid installing Python dependencies "globally" - In other words, we make sure not to leave the power drill on the kitchen counter for no reason at all.

So how do we use this tool?

Well, we start from the command line. In your VS Code terminal open up the folder for your Python projects and run this command:

`python3 -m venv venv`

This uses a Python 3 module  `venv`

Mac/Linux
`source venv/bin/activate`

Windows:
`venv\Scripts\activate`

`pip install requests`

### Using APIs!

```py
import json
import requests
import urllib.parse

YOUR_EMAIL = "replace_with@your_email.com"

encoded_email = urllib.parse.quote_plus(YOUR_EMAIL)

url = "https://haveibeenpwned.com/api/v2/breachedaccount/" + encoded_email

response = requests.get(url)
data = json.loads(response.text)

for i in data:
    print("My data is in the " + i['Name'] + " breach. Yikes!")

```



## [Next... Part 6](part6.md)

### [Previous... Part 4](part4.md)