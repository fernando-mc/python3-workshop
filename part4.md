# A Complete Beginner's Introduction to Python

## Part 4

### Flow Control

Now that we know how to check if something is `True` or `False`, we can use this to make Python execute commands conditionally.

```python
if 6 > 5:
     print("Six is greater than five!")
```

That was our first multi-line piece of code, and the way to enter it at a Python prompt is a little different.

1. First, type the `if 6 > 5:` part, and hit `enter`. The next line will have `...` as a prompt, instead of the usual `>>>`. This is Python telling us that we are in the middle of a code block, and so long as we indent our code it should be a part of this code block.
2. Type 4 spaces, type `print("Six is greater than five!")`, and then hit `enter` to end the line. 
3. Finally, hit `enter` again to tell Python you are done with this code block. All together, it will look like this:

```python
>>> if 6 > 5:
...      print("Six is greater than five!")
Six is greater than five!
```

So what's going on here? When Python encounters the `if` keyword, it evaluates the expression following the keyword and before the colon. If that expression is `True`, Python executes the code in the indented code block under the `if` line. If that expression is `False`, Python skips over the code block.

In this case, because 6 really is greater than 5, Python executes the code block under the if statement, and we see "Six is greater than five!" printed to the screen. Guess what will happen with these other expressions, then type them out and see if your guess was correct:

```python
if 0 > 2:
     print("Zero is greater than two!")
```

```py
if "Prince" in "The Artist Formerly Known As Prince.":
    print("Dance on.")
```

#### if and else

You can use the `else` keyword to execute code only when the `if` expression isn't `True`:

```py
sister_age = 15
brother_age = 12
if sister_age > brother_age:
    print("sister is older")
else:
    print("brother is older")
```

Like with `if`, the code block under the `else` statement must be indented so Python knows that it is a part of the `else` block.

#### compound conditionals: `and` and `or`

We've been testing single conditions, but we can also test multiple conditions that result in execution of some code. You can check multiple expressions together using the `and` and `or` keywords. 

- If two expressions are joined by an `and`, they both have to be `True` for the overall expression to be `True`. 
- If two expressions are joined by an `or`, as long as at least one is `True`, the overall expression is `True`.

Try typing these out and see what you get:

```py
1 > 0 and 1 < 2
1 < 2 and "x" in "abc"
"a" in "hello" or "e" in "hello"
1 <= 0 or "a" not in "abc"
```

Guess what will happen when you enter these next two examples, and then type them out and see if you are correct. If you have trouble with the indenting make sure to use a consistent number of spaces when typing things out. Indenting is a crucial part of Python syntax so you'll want to get more comfortable with as you continue to write Python code.

```py
temperature = 32
if temperature > 60 and temperature < 75:
    print("It's nice and cozy in here!")
else:
    print("Too extreme for me.")
```

```py
hour = 11
if hour < 7 or hour > 23:
    print("Go away!")
    print("I'm sleeping!")
else:
    print("Welcome to the cheese shop!")
    print("Can I interest you in some choice gouda?")
```

You can have as many lines of code as you want in if and else block; just make sure to indent them so Python knows they are a part of the block.

#### Even more choices: `if`, `elif`, and `else`

If you have more than two cases, you can use the `elif` keyword to check more cases. Think of `elif` as Python-speak for else if. You can have as many `elif` cases as you want. Python will go down the code checking each `elif` until it finds a `True` condition or reaches the default `else` block.

```py
sister_age = 15
brother_age = 12
if sister_age > brother_age:
    print("sister is older")
elif sister_age == brother_age:
    print("sister and brother are the same age")
else:
    print("brother is older")
```

You don't have to have an `else` block if you don't need it. That just means there isn't default code to execute when none of the `if` or `elif`conditions are `True`:

```py
color = "orange"
if color == "green" or color == "red":
  print("Christmas color!")
elif color == "black" or color == "orange":
  print("Halloween color!")
elif color == "pink":
  print("Valentine's Day color!")
```

If color had been "purple", that code wouldn't have printed anything.

*Remember that `=` is for assignment and `==` is for comparison.*

### Functions

Functions take input from the user or the application and (usually) produce output (e.g. they return a value). You can then assign a variable to this output. As we've shown in previous sections, you call a function by using its name followed by its arguments in parenthesis.

Why are functions important?

* They allow tasks to be run quickly and to be automated, i.e. they do some useful bit of work.
* They let us re-use code without having to type it out each time.
* They facilitate consistency and reduce the risk of error. 

Python has many built in functions. For example:

```py
length = len("Mississippi")
```

Executing this code assigns the length of the string "Mississippi" to the variable `length`. We can write our own functions to encapsulate bits of useful work so we can reuse them. Here's how you do it:

#### Step 1: Write a Function signature

A function signature tells you how the function will be called. It starts with the keyword `def`, which tells Python that you are defining a function. Then comes a space, the name of your function, an open parenthesis, the comma-separated input parameters for your function, a close parenthesis, and a colon. 

Here's what a function signature looks like for a function that takes no arguments:

```py
def myFunction():
    # Your code would go here!
```

Here's what a function signature looks like for a function that takes one argument called `my_string`:

```py
def myFunction(my_string):
```

And one for a function that takes two arguments:

```py
def myFunction(my_string, myInteger):
```

Parameters should have names that usefully describe what they are used for in the function. 

**Note:** The words parameters and arguments are seemingly interchangeable in reference to the input to functions. The distinction isn't really important right now, but if you're curious: in function signatures the input is called parameters, and when you are calling the function the input is called arguments.

#### Step 2: Do useful work inside the function

Underneath the function signature is where you do your useful work. Everything inside the function is indented, just like with if/else blocks, so Python knows that it is a part of the function. You can use the variables passed into the function as parameters, just like you can use variables once you define them outside of functions.

```py
def add(x, y):
    result = x + y
```

#### Step 3: Return something

If you want to be able to assign a variable to the output of a function, the function has to return that output using the `return` keyword.

```py
def add(x, y):
    result = x + y
    return result
```

or, even shorter:
```py
def add(x, y):
    return x + y
```

You can return any Python object: numbers, strings, booleans, and even other functions! Once you execute a return, you are done with the function -- you don't get to do any more work. That means that if you have a function like this:

```py
def absoluteValue(number):
    if number < 0:
        return number * -1
    return number
```

If `number` is less than 0, you return number * -1 and never even get to the last line of the function. However, if number is greater than or equal to 0, the if expression evaluates to False, so we skip the code in the if block and return number.

We could have written the above function like this if we wanted. It's the same logic, just more typing:

```py
def absoluteValue(number):
    if number < 0:
        return number * -1
    else:
        return number
```

#### Step 4: Use the function

Once you define a function you can use it as many times as you want. You can assign the value it returns to other variables and use those variables in other commands.

```py
def add(x, y):
    return x + y
```

```py
result1 = add(1234, 5678)
print(result1)
result2 = add(-1.5, .5)
print(result2)
print("The total sum is", result1 + result2)
```

Functions don't have to return anything if you don't want them to. They usually return something because we usually want to be able to assign variables to their output. If your function does not return anything, you won't be able to assign a variable to its output and won't be able to use its output anywhere else.

What do you think will happen here? Try it and see:

```py
def half_number(x):
    print(x/2)

half1 = half_number(20)
print(half1)
```

## [Next... Part 5](part5.md)

### [Previous... Part 3](part3.md)