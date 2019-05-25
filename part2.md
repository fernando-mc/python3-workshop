# A Complete Beginner's Introduction to Python

## Part 2

### Variables

Variables are critical parts of working with Python and many other programming languages. Variables have an "identifier" (which is the variable's name) and a value that is stored in the variable. The value doesn't just have to be a number like integers or floats it can be many other things too!

In the example below, `x` is our identifier and `4` is the value stored:

```python
type(4)
x = 4
x
type(x)
2 * x
```

Giving a name to something so that you can refer to it by that name later is called assignment. Above, we assigned the name `x` to 4, and after that we can use `x` wherever we want to use the number 4.

The space between the identifier, the equal sign, and its value does not matter. The two variables below are identical. However, you should try to be consistent with how you assign variables in your code to keep things stylistically consistent.

```python
x = 5
x=5
```

Variables can also be re-assigned.

```python
x = 3
x
x = 7
x
```

Be careful when you do this though... accidentally re-assigning a variable can cause bugs in your code.

A variable’s identifier can contain letters, numbers, and underscores. However, identifiers must start with a letter and can not contain any other special characters. Here are some valid variable names:

```python
days_in_year = 365
kilosOfRice = 1.75
first_name = "Fernando"
```

Projects develop naming conventions, so multi-word identifiers may use underscores (like `days_in_year`), or "camel case" (like `kilosOfRice`). The most important thing is to be consistent within a project, because it makes the code more readable.

### Strings

So far we’ve seen two data types: *integers* and *floats*. Another useful data type is a *string*, which is just what Python calls a bunch of characters (like numbers, letters, whitespace, and punctuation) put together between quotation marks:

```python
"Hello"
"Python, I'm your #1 fan!"
```

Just like with the numeric data types, we can check the type of a string:

```python
type("Hello")
type(1)
type("1")
```

You can assign a string value to a variable:

```python
my_car_brand = "Mazda"
```

### String Concatenation

You can concatenate (join) strings together using the `+` sign:

```python
"Hello" + "everyone,"
"I drive a " + my_car_brand
```

You can't concatenate a string with another data type.

```python
"Hello" + 123
```

Trying to do this will give you a *traceback*:

```
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

A traceback provides details on what was happening when Python encounters an Exception or Error – something it doesn’t know how to handle. There are many kinds of Python errors, each with descriptive names to help us humans understand what went wrong. In this case we are getting a `TypeError`: we tried to do some operation on a data type that isn’t supported for that data type.

Python gives us a helpful error message as part of the TypeError:

```
"cannot concatenate 'str' and 'int' objects"
```

We can, however, use the `str()` function to convert a number to a string. Like the `type()` function we’ve been using, `str()` takes one argument as input and outputs it as a string.

```python
str(4)
str(5.34)
str("Ice cream")
```

### Sting Length

There’s another useful function that works on strings called `len()`. This returns the length of a string as an integer.

```python
len("Hello")
len("")
performer = "Prince"
len(performer)
```

### Quotes

We've been using double quotes around your strings, but either double or single quotes are valid in Python:

```py
'Hello world'
"Hello world"
```

You do have to be careful about using quotes inside strings. Something like this...

```py
'Let's learn Python together!'
```

... will give you another `traceback`, for a `SyntaxError`. When Python evaluates this expression, it starts at the first single quote as the start of the string, and to the next single quote as the end of the string. Then it doesn't know what to do with the rest of the stuff that follows.

There are a few ways to solve this problem. One is to use double quotes on the outside:

```py
"Let's learn Python together!"
```

or we can *escape* the quote with a backslash:

```py
'Let\'s learn Python together!'
```

The backslash is a special character that tells Python to treat the next character literally, not as part of the syntax or code. Thus, you can do things like this:
```py
sentence = "Fernando said, \"Python is fun!\""
print(sentence)
```

*By the way, in Python 3, print is another function that prints out a string for us!*

### Practice Exercises

Let's take a look at a couple of exercises. Read the following lines of code, but don't execute them! Try to figure out what they will do. Write them out on paper or type them out in a text document if you need to. Then type them in your terminal and execute them to see what happens.

1.

```py
total = 1.5 - 1/2 + ((-2.0/2) - (1.0/2))
print(total)
type(total)
```

2.

```py
a = "quick"
b = "brown"
c = "fox jumps over the lazy dog"
print("The " +  a * 3 + " " +  b * 3 + " " + c)
```

3.

```py
print(2.0 * 123 + str(2.0) * 123)
```


## [Next... Part 3](part3.md)

### [Previous... Part 1](part1.md)