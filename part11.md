# A Complete Beginner's Introduction to Python

## Part 11

### Amazon Web Services (AWS) and Software Development Kits (SDKs)

AWS is a part of Amazon that offers different "cloud services". These cloud services allow you to extend the functionality of your applications with everything from virtual machines to databases and other application development tools. If you leverage these tools with your applications you'll also probably end up writing code in a programming language to interact with the services. When you do this, you'll want to leverage a software development kit or SDK. 

SDKs make it easier to interact with some application functionality usually by providing you some sort of package that contains code that makes doing typical operations with the tool or service easier. For example, they might have built-in support for all the things that need to happen in the background to authenticate correctly with a service or to .

#### Getting Started with the AWS SDK for Python - boto3

The first step to working with an SDK is to go out and get it! With Python, we can install the AWS SDK for Python (boto3) using `pip`. We can install it in our virtual environment using `pip install boto3`. This should install boto3 and all of the packages it requires.

After we have it installed, we can open up the Python interpreter and confirm this by running `import boto3`. With that done we can `exit()` back out of the Python interpreter and continue with a few more required steps. 

When we're working with AWS and boto3 we'll need to have a way to authenticate ourselves to AWS and prove that we have permission to do things we want to do. This process would normally involve:

1. Creating your own AWS Account 
2. Creating an AWS user with access keys and permissions for the actions you'd like to take with AWS
3. Setting up the AWS Command Line Interface (CLI)
5. Configuring the AWS Access keys using the AWS CLI

Go ahead and follow along with the instructions in the links above and then we can continue using boto3 in our next project!

#### Using boto3 to Interact with Amazon Translate

Now that we've done all that setup work, let's go ahead and try using boto3!

```python
import boto3

def translate(user, message):
    # Create a client and don't give it away for free
    translate_client = boto3.client(
        'translate',
        region_name='us-east-1'
    )
    # Take user and figure out language they want
    users = {
        "Fernando": "es", 
        "UserOne": "ja", 
        "UserTwo": "de",
    }
    language = users[user]
    # Translate input message to language
    translated_message = translate_client.translate_text(
        Text=message,
        SourceLanguageCode='en',
        TargetLanguageCode=language
    )
    # Return the translated result
    return translated_message["TranslatedText"]
```

## [Now What?](nowwhat.md)

### [Previous... Part 10](part10.md)