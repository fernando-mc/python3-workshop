# A Complete Beginner's Introduction to Python

## Part 8

### for Loops

We can use `for` loops to run a bit of code for every part of an iterable Python value. Iterables are basically things that can be broken up into parts in Python. For example, a list or tuple can be broken up into all the elements in the list. A string can be broken up into all of the characters inside of it.

Here's how we write a basic `for` loop:

```python
for number in [1,2,3]:
    print(number)
```

We use the keyword `for` to signify the start of the loop. Then we provide a name that will carry the value of the iterables in the code within our loop, in this case `number` (but we could use any word that is an allowed variable name). After that, we use the `in` keyword to specify what we are iterating over, in this case, a three element list.

On the next line, we indent the same way we would with a function definition or an `if` block and we type out the code we want to execute for each value in the list. In this case, it just prints out the numbers 1, 2, and 3. 

But what happens in this case:

```python
for thing in "hello":
    print(thing)
```

Try it out! You'll notice that the letters themselves are iterated through and printed out. You'll also notice that we used `thing` to reference the individual iterable values. We could have used `flamingo` or any other valid variable name.

Just like with other examples, we can define variables and use them in the place of the values we used earlier.

```python
numbers = [1,2,3]
for number in  numbers:
    print(number)
```

Try writing your own `for` loop in order to add up the numbers in this list: `[10, 3, 412312, 5123, 1231, 5342]`


### while Loops

In addition to `for` loops, which loop through the values in an iterable object, we can also use `while` loops which keep looping *while* a condition is True.

For example, we could write an infinite loop!

```python
while True:
    print("press Control + C to stop me!")
```

Because the condition of the while loop is simply `True` it will run and run forever. But what if we wanted to run a loop for a specified amount of attempts? In that case we can do a little setup beforehand.

```python
counter = 0
while counter < 5:
    print("counter is at: " + str(counter))
    counter = counter + 1
```

This allows us to run this loop a set number of times while the `counter` variable approaches 5.

### Nested Loops

We can also combine these approaches and even use `if` too!

```python
people = ["Prince", "Sam", "Mo", "Em"]
for person in people:
    if person == "Prince":
        print("Ahhhhh! It's Prince - Let Prince in!")
    else:
        print("Hello, " + person + ". Welcome to the conference")
```

Try writing your own nested loops! Use a for and a while loop to print out a list three times.

### range, break, input

The `range()` function allows us to create a a range object that represents a list of numbers. Range can take up to three arguments: start, stop, step. Start is the integer where the range should begin, stop is where the range stops and is non-inclusive and step is how big the difference between the numbers in the range should be. 

Let's take a look at an example:

```python
range(0,10,2)
```

Now, if that's all you type in, Python doesn't expand the range into a list. It's treated as a separate object type because it's just a different way of representing the same thing. If you want to see the individual numbers you'll need to *cast* the range to a list. You've done this before with `str()`. 

To case a range to a list all you have to do is wrap it in `list()`. For example:

```python
list(range(0,10,2))
```

This gives us: `[0, 2, 4, 6, 8]`. The range said start at 0 (including zero) then go all the way up to ten but don't include it, and jump up by two.

Try making a few more ranges yourself. Now notice what happens when I make a range like this:

```python
list(range(10))
```

It works! And outputs something that starts at zero and goes up by one. That's because when we only provide one value the `range()` function assumes we want to start at zero and go up by one.

We can also use two values:

```python
list(range(2, 10))
```

This will assume that the first value is the start and the second value is the stop. So, depending on how many values we put in, Python will assume the values mean different things:

- One value: stop
- Two values: 1) start, 2) stop
- Three values: 1) start, 2) stop, 3) step

### break

Using the `break` keyword is another way to end a loop.

```python
i = 1
while True:
    i += 1
    if i == 3:
        break
    else: 
        print("Keep going!")
```

### input

If you want to write a Python program and want a simple way to ask for input from a user you could use `input()`. Realistically, there are many other tools you'd end up using to get user input depending on the context of what you're building ot working with. But this is an easy way:

```python
your_name = input("Hello, what is your name?")
print("Hello, " + your_name + ", nice to meet you!")
```

This makes much more sense in the context of running a Python script so let's paste the above code into a new file - `greeting.py` and then run the file.

## [Next... Part 9](part9.md)

### [Previous... Part 7](part7.md)