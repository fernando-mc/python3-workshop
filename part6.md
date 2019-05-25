# A Complete Beginner's Introduction to Python

## Part 6

### Web APIs Explained

APIs or Application Program Interfaces allow different programs to communicate with one another. Web APIs are a subset of APIs that are accessible through the internet. 

APIs can be incredibly useful when we're building applications in order to extend the data or functionality we have access to in our applications. We're going to be using an API in the project we'll be working on below to find out if our email addresses have ever been in a data breach.

The specific API we'll be using is called "[Have I Been Pwned](https://haveibeenpwned.com)" and was created by digital security expert [Troy Hunt](https://www.troyhunt.com/about/). This API allows us to provide it an input of our email and then, if our email was in historical data breaches, it returns what breaches our passwords or other information was exposed in.

Let's take a look at how we can use it!

### Using the Have I Been Pwned API!

The first thing we'll want to do is open up our Python interpreter in the VS Code terminal and import some dependencies:

```py
import requests
import urllib.parse
```

So we imported both `requests` and this weird `urllib.parse` thing. Well, that's importing a part of the `urllib` library - `parse`. Next up, let's add our actual emails in a variable and modify it slightly using `urllib`:

```python
YOUR_EMAIL = "replace_with@your_email.com"
encoded_email = urllib.parse.quote_plus(YOUR_EMAIL)
```

After we save the email as `YOUR_EMAIL` we then create a new variable called `encoded_email`. We do this by using a handy method called `quote_plus` inside of `urllib.parse`. It will change a Python string of an email like `"fernando@gmail.com"` to `"fernando%40gmail.com"`. I wont go into the details about this here, but basically the `%40` is equivalent to the `@` symbol - but `%40` isn't going to break anything if we send it to the API we're using.

Next up, we create the url that we'll use to get the information from the API using string concatenation and adding the encoded email to the base URL (that I've included for you below):

```python
url = "https://haveibeenpwned.com/api/v2/breachedaccount/" + encoded_email
```

Next up, let's use `requests` to make a request to that URL similar to how we would with a web browser like Chrome or Firefox. We'll use `requests.get(url)` to do this, but we'll save the response in a variable called `response`. Then we'll look at the text of the response by running `response.text`:

```python
response = requests.get(url)
response.text
```

At this point, if you don't see anything - Don't worry! You can troubleshoot this by running `print(url)` to print out the URL and then try pasting it into a web browser. If you see information, then the email you provided was included in a breach and should also have produced some output when you ran `response.text`. 

If you don't see any information, you're one of the lucky few of us who has never had their email compromised in a data breach! You can try this whole process again with the email `joe@gmail.com` to feel our pain.

The result of `response.text` is a big string of information in a format called JSON. But if you peek closely at it you can see the name of the breach and other details related to it. Congratulations! You just learned how to use your first API with Python!

If you want to learn more about how to dig deeper into this data I'll leave a few suggested readings at the end of this tutorial!

### Bonus Project... Using Software Development Kits (SDKs) and "the cloud"! ☁️

First, you'll need to exit the Python interpreter and install a new package called `boto3` with `pip`. Remember - you just did this with `requests`, give it a shot now! If you need help, just ask!

Next, with `boto3` installed, open that Python interpreter back up and ask the instructor where to get the special keys you can use for this demo.

Then, replace the values of the strings of the three capitalized variable names and then copy this code into your interpreter!

After you've run it all once, try running `frenchify` with your own sentence to translate. Or maybe, try and write yourself a `spanishify` function. I'll give you a hint... the Spanish language code is `es`. 

```python
import boto3

TEXT_TO_TRANSLATE = "Whatever you'd like!"
ACCESS_KEY = ""
SECRET_ACCESS_KEY = ""

translate = boto3.client(
    "translate",
    aws_access_key_id=ACCESS_KEY,
    aws_secret_access_key=SECRET_ACCESS_KEY,
)

def frenchify(text):
    result = translate.translate_text(
        Text=text, 
        SourceLanguageCode="en",
        TargetLanguageCode="fr"
    )
    print(result.get('TranslatedText'))

frenchify(TEXT_TO_TRANSLATE)
```

Note: This project is a bit more advanced with some new concepts, don't be afraid to try things out. Also note that in order to do this project past the time of the workshop you will need to create your own [AWS account](https://aws.amazon.com/).

So what next?! Let's find out.

## [Next... Now What?](nowwhat.md)

### [Previous... Part 5](part5.md)