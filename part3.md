# A Complete Beginner's Introduction to Python

## Part 3

### Comments and New Lines

Below is an example of how to use comments and insert new lines:

```python
# The pound sign is used as a comment character in Python. Programmers
# use comments to annotate code. Python ignores everything after the
# comment character on a line. (unless the # symbol is in a string)

# Notice how the 'print' command has been inserting a new line at the
# end of our strings.
print("The best three prince songs are:")

# We can insert newlines ourselves, using "\n".
print("Purple Rain\nWhen Doves Cry\nI Would Die 4 U")

# "" Is the empty string. Since the print command will insert a
# newline at the end, this will print a newline by itself:
print("")

# Here's a new kind of printing: you can use triple quotes to create
# multiline strings.
print("""Prince Rogers Nelson was an American singer, songwriter, 
musician, record producer, actor, and filmmaker. 
With a career spanning four decades, Prince was known for his
eclectic work, flamboyant stage presence, extravagant fashion 
sense and use of makeup, and wide vocal range.""")

print("")

# When you use triple quotes, whitespace is preserved.
print("""Prince was born 
    in Minneapolis, 
        Minnesota.""")
```

### Python Scripts

So far, we've been running code directly from the Python shell interpreter (the `>>>` prompt). This is great for testing and exploring short bits of code, but for longer projects we want to save our script in a file and run it from our terminal.

1. Create a new file in VS Code in the `workshop2019` directory on your desktop called `prince.py`. Note the `.py` file extension, indicating that this is a Python script.
2. Copy the entire code block from the previous section (including the comments) and use VS Code to open and edit the file and paste it into `prince.py`. 
3. Save the file with VS Code
4. In the VS Code Terminal type `exit()` into the Python interpreter and press enter. Then, make sure you navigate to the folder containing your `prince.py` file. 
5. Once you think you're in that folder use either `ls` or `dir` (depending on your operating system) to see the files in that folder and confirm that one of them is `prince.py`.
6. Then, type out:
    - `python3 prince.py` (On Mac/Linux) or 
    - `py prince.py` (On Windows)

and press enter to run this script. Study what happens. Then go ahead and edit this file so it displays another Prince song (Look them up on [Wikipedia](https://en.wikipedia.org/wiki/Category:Prince_(musician)_songs) if you need to!). Save it and run it again.

**Celebration of Learning! (AKA, a quiz)**

- How do you run a Python script from your computer's terminal?
- How do you comment code in Python?
- How do you print just a newline?
- How do you print a multi-line string so that whitespace is preserved?

### Booleans

So far, the code we've written has been *unconditional*: no choice is getting made--all of the code runs. Python has another data type called a **boolean** that is helpful for writing code that makes decisions. Booleans hold two values: `True` and `False`.

Re-open the Python interpreter and try typing these:
```python
True
type(True)
False
type(False)
true
false
```

What happens? What's going on with `true` and `false`? Well, they're not actually boolean values. Only `True` and `False` are booleans in Python. 

You can test if Python objects are equal or unequal. The result is a boolean. Try typing these expressions in your Python console:

```python
0 == 0
1 == 0
54 = 42
```

Use `==` to test for equality. Recall that `=` is used for assignment of a variable to a value. This is an important idea and can be a source of bugs until you get used to it: `=` is assignment, `==` is comparison.

Use `!=` to test for inequality:

```python
"a" != "a"
"a" != "A"
```

`<`, `<=`, `>`, and `>=` have the same meaning as in math class. The result of these tests is a boolean:

```python
1 > 0
2 >= 3
-1 < 0
.5 <= 1
```

You can check for containment with the `in` keyword, which also results in a boolean:

```python
"H" in "Hello"
"X" in "Hello"
```

Or check for a lack of containment with `not in`:

```py
"a" not in "abcde"
"JavaScript" not in "Python Workshop"
```

Awesome! Knowing how to compare things, along with using booleans and equality will enable us to determine if we should run different bits of code later on depending on these different conditions!

## [Next... Part 4](part4.md)

### [Previous... Part 2](part2.md)