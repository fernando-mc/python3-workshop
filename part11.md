# A Complete Beginner's Introduction to Python

## Part 11

### Amazon Web Services (AWS) and Software Development Kits (SDKs)

AWS is a part of Amazon that offers different "cloud services". These cloud services allow you to extend the functionality of your applications with everything from virtual machines to databases and other application development tools. If you leverage these tools with your applications you'll also probably end up writing code in a programming language to interact with the services. When you do this, you'll want to leverage a software development kit or SDK. 

SDKs make it easier to interact with some application functionality usually by providing you some sort of package that contains code that makes doing typical operations with the tool or service easier. For example, they might have built-in support for all the things that need to happen in the background to authenticate correctly with a service or to .

#### Getting Started with the AWS SDK for Python - boto3

The first step to working with an SDK is to go out and get it! With Python, we can install the AWS SDK for Python (boto3) using `pip`. We can install it in our virtual environment using `pip install boto3`. This should install boto3 and all of the packages it requires.

After we have it installed, we can open up the Python interpreter and confirm this by running `import boto3`. With that done we can `exit()` back out of the Python interpreter and continue with a few more required steps. 

When we're working with AWS and boto3 we'll need to have a way to authenticate ourselves to AWS and prove that we have permission to do things we want to do. This process would normally involve:

1. [Creating your own AWS Account](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/)
2. [Creating an AWS user with access keys and permissions for the actions you'd like to take with AWS](https://docs.aws.amazon.com/translate/latest/dg/setting-up.html)
3. [Setting up the AWS Command Line Interface (CLI)](https://docs.aws.amazon.com/translate/latest/dg/setup-awscli.html)
5. [Configuring the AWS Access keys using the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html)

Go ahead and follow along with the instructions in the links above and then we can continue using boto3 in our next project!

#### Using boto3 to Interact with Amazon Translate

Now that we've done all that setup work, let's go ahead and try using boto3!

Let's pretend we want to create a Python function that will translate text for us depending on the user we want to send it to. In this example, we have three users: "Fernando" wants text in Spanish, "Dieter" wants it in German, and Ai would like it in Japanese. Let's see how we might do that with boto3 and the Amazon Translate service.

We'd start by importing boto3 to use in the interpreter:

```python
import boto3
```

Then, we'd create a "client" to let us interact with the Amazon Translat service and call it `translate_cleint`.

```python
translate_client = boto3.client(
    'translate',
    region_name='us-east-1'
)
```

Then, we can create a dictionary to store the language preferences of our users with a two character language code.

```python
user_languages = {
    "Fernando": "es", 
    "UserOne": "ja", 
    "Dieter": "de",
}
```

Finally, we can use these parts to output a translation of the words "Hello friends!" into Dieter's preferred language:

```python
translate_client.translate_text(
    Text="Hello friends!",
    SourceLanguageCode='en',
    TargetLanguageCode=user_languages["Dieter"]
)["TranslatedText"]
```

The above code uses the Amazon Translate client created by boto3 and the expected arguments [defined in the boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/translate.html#Translate.Client.translate_text) and then specifically returns the "TranslatedText" portion of the full response because we add `["TranslatedText"]` on the end of the `translate_text` method we use.

All together, if we put together our code in a file and moved it inside of a function to be more reuseable it might look like this:

```python
import boto3

def translate(user, message):
    # Create a client and don't give it away for free
    translate_client = boto3.client(
        'translate',
        region_name='us-east-1'
    )
    # Take user and figure out language they want
    user_languages = {
        "Fernando": "es", 
        "UserOne": "ja", 
        "Dieter": "de",
    }
    language = user_languages[user]
    # Translate input message to language
    translated_message = translate_client.translate_text(
        Text=message,
        SourceLanguageCode='en',
        TargetLanguageCode=language
    )
    # Return the translated result
    return translated_message["TranslatedText"]
```

With this code, try pasting it into a new file called `translator.py`. Then open the interpreter in the same directory as this function and run:

```python
import translator
```

This should bring the contents of `translator.py` into the interpreter. You will then need to use `translator.` to reference things inside that file. For example, we could use the function written in the file like this:

```python
translator.translate("Fernando", "Hello friend!")
```

And this should return the translated version of the text in Spanish! Try playing around with this and adding a few more Language codes and translations!

## [Now What?](nowwhat.md)

### [Previous... Part 10](part10.md)