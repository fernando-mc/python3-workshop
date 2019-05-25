# A Complete Beginner's Introduction to Python

## Part 1

With Python v3.7.3 and VS Code installed we can get started learning Python!

As you go through this guide, you will see different sections that look like this:

`my_name = "Fernando"`

You'll find similar fonts to this throughout the internet when looking at programming guides. That sort of font style indicates that it is code of some sort. In this particular guide, it will usually reference Python code that we can enter into the Python interpreter.

So, with the above example, type our the line of code at the `>>>` prompt in your Python shell. Simply type the code out and then hit Return or Enter after every line and then note the output (although sometimes there won’t be any!).

Important: For now, don’t copy and paste any commands. When you type them out by hand you'll learn a lot more!

### Math

In Python, math looks very similar to math with a calculator.

#### Addition

```python
5 + 5
1.5 + 3.1
2 + 1.65
```

#### Subtraction

```python
25 - 5
36.12 - 3.12
6 - -4
```

#### Multiplication

Multiplication operations use the `*` symbol. It is called an asterisk or star symbol. The character `x` has no mathematical purpose in Python though it is sometimes used as a variable name (more on variables later).

```python
3 * 12
1.2 * 4.7
.5*10
6 * -2
```

#### Division

Division uses the `/` symbol. 

```python
24 / 2
15 / -5
13/6
```

In Python 2 division works a little differently than in Python 3. Python 2 would return whole numbers using something called "Floor division". In Python 3 you'll see the true value of the result with a decimal.

If you wanted to use floor division in Python 3 you could use the `//` operator.

```python
16//3
50//4
```

#### Modulus

Remember using long division and getting stuck with a "remainder" after doing the division? If you want the remainder in Python you can use the modulus operator. The symbol for this is the percent symbol: `%`.

```python
4%3
38%6
```

#### Exponents

You can also use the double asterisk operator to signify exponents.

```python
2 ** 4
2 * 2 * 2 * 2
3 * 3
3 * 3 * 3
```

### Order of Operations

The order of operations in Python is exactly the same as it was in your math classes! If you remember, the acronym PEMDAS (Parentheses, Exponents, Multiplication, Division, Addition, Subtraction) determines the order operations will take place in.

```python
2 + 4 * 10
(2 + 4) * 10
2 ** 2 + 2
2 ** (2 + 2)
```

### Types

Because we jumped straight into some of the basics of Python math, we skipped over a few concepts, including the concept of types. In Python, the different things we work with have "types". We can use a helpful Python function (more on functions later!) called `type` that allows us to find out what types the things we're working with are. Here's how:

```python
type(1)
type(1.0)
```

The first of the lines returns `<class 'int'>` which tells us the value of `1` is an integer. The second line returns `<class 'float'>` which tells us the value of `1.0` is another data type completely - a float!

I also mentioned "functions" without explaining what those are. We'll write and use functions more later, but for now realize that:

- Functions do some useful work for us so that we don’t have to type it out repeatedly. In this case, the `type` function helps us do the work of finding the type of an object easily.
- You can provide a function an input and from there it can produce an output. In this case, the `type` function took our input and then told us the data type.
- When we use functions, we write the name of the function and then an open parenthesis, then we put in any input(s) to function that are required (these are called arguments) and finally we end with a closing parenthesis.

In the case above, `type` is the name of the function, and it takes one argument (the thing we want to figure out the type of). We first gave it an argument of `1` and then give it an argument of `1.0`.

### Python Command History

Before we move on to the next section, try pressing the up arrow key on your keyboard. Python should remember the previous things you typed and show them to you! This can be especially useful if you want to go back to previous line and rerun it or fix something before running it again.

## [Next... Part 2](part2.md)

### [Previous... Navigating with a Terminal](navigating-with-a-terminal.md)