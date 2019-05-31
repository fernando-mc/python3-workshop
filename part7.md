# A Complete Beginner's Introduction to Python

## Part 7

### Lists

Whenever you go to the grocery store you probably bring a shopping list along with you. Well the Python developers created a whole data type just for you called *lists*. Single values like strings, integers, and floats can all be useful by themselves but we frequently need to organize our things together to be useful. That's where lists come in. Lists are used to store other things and can contain any data types. You may also hear lists referred to as arrays, inside of Python, these two words mean the same thing.

#### Creating Lists

The same way that strings are enclosed in quotations, lists are enclosed in square brackets: `[]`. All of the values inside of a list are separated by commas and lists can have zero or more values. For example:

- An empty list: `[]`
- A one-value list with an integer: `[37]`
- A two-value list with an integer and string: `[37, "Purple Rain"]`

The easiest way to start working with lists is to create a list and assign it to a variable:

```python
prince_songs = ["I Would Die 4 U", "Purple Rain", "When Doves Cry"]
```

If we check the type on this new variable we'll see it has a type of `list`:

```python
type(prince_songs)
```

We can also use the built in `len()` to get the length of our list:

```python
len(prince_songs)
```

This shows that our list has three elements inside of it - three strings containing titles of Prince songs. 

#### Accessing Lists

So what if we want to access the things in our list? Well, we can do this simply by referencing the position of the element we want. We do this with square brackets and a number:

```python
prince_songs[1]
```

Whoa! Hold on here, that output "Purple Rain". That was the second element in our list. What happened here? Well, many different programming languages including Python actually start counting from zero in situations like this. So if we wanted the first item in the list we would need to do this instead:

```python
prince_songs[0]
```

But what if we had a really long list and we knew we needed something a few places from the end of the list? Well, Python makes it easy for us to do that too. We can reference the list counting from the back with a negative integer.

```python
prince_songs[-1]
```

I know, I know. I just told you that we start counting at zero when we work with lists. So why does referencing negative one give us the last item in the list? Well that's because when we're counting backwards we do actually need to start at one. The reason for this is because negative zero just doesn't make much sense - it's the same thing as zero. So in this case if you wanted the second from the last element you could reference it with 

```python
prince_songs[-2]
```

In short, to reference a list, start at 0 from the left. Start at -1 from the right.

#### Adding and Removing List Elements

So let's say we have another list and we store it in a variable called `groceries`:

```python
groceries = ["fruit", "yogurt"]
```

What happens if we want to add a new item `"burrito"` to the end of our grocery list? Well, that's called *appending* items to our list. We can do this using the following syntax:

```python
groceries.append("burrito")
```

We could also append a variable:

```python
x = "salsa"
groceries.append(x)
```

Now if we type in `groceries` and hit enter our list looks like this: `['fruit', 'yogurt', 'burrito', 'salsa']`. What if we wanted to add something to our list at a particular spot in the list? In that case we can use `insert`:

```python
groceries.insert(1, "carrots")
```

Now `groceries` looks like this: 

```python
['fruit', 'carrots', 'yogurt', 'burrito', 'salsa']
```

If we want to remove an element we can use `remove()`.

```python
groceries.remove("salsa")
```

Now we have: `['fruit', 'carrots', 'yogurt', 'burrito']`. If we wanted to remove a specific value from the list we could use `remove()`. 

```python
groceries.remove("carrots")
```

Now this gives us `['fruit', 'yogurt', 'burrito']` as we expect. But what if our groceries list looked a little different when we used remove:

```python
groceries = ['fruit', 'carrots', 'yogurt', 'burrito', 'carrots']
groceries.remove("carrots")
```

In this case, we still end up with some carrots on our list: `['fruit', 'yogurt', 'burrito', 'carrots']`. This is because `remove()` only removes the first instance of a matching element in our list. 

If we wanted to remove an element at a particular part of the list we can use `pop`. By default, `pop` will remove the last value from our list and return it to us. 

```python
groceries = ['fruit', 'yogurt', 'burrito', 'carrots']
groceries.pop()
```

The above code would change the groceries list to be `['fruit', 'yogurt', 'burrito']` and it would also return `'carrots'` to us. But in addition to `pop`ing the final element of a list we can also we can also specify that it remove and return a value at a particular position in our list. For example, running `groceries.pop(1)` would remove `'yogurt'` from the list and return it to us.

#### Slicing and Copying Lists

How else can we interact with lists? Lists allow us  themselves using *slicing*. Slicing a list returns a copy of the list and allows us to specify what range of elements in the list we'd like.

To slice a list, you can use syntax similar to the square brackets that you would normally use to reference a specific element. The syntax is structured like this:
`[Start Point:End Point]`. The start and end point must be integers and while the start point is inclusive the end point is not.

Here are a few examples of the syntax in action:

```python
my_numbers = [0, 1, 2, 3, 4, 5, 6]
all_numbers = my_numbers[:]
first_three_numbers = my_numbers[:3]
last_three_numbers = my_numbers[-3:]
middle_three_numbers = my_numbers[2:5]
```

Go ahead double check what's in each of these results and see if you can practice manipulating this new list yourselves:

```python
days = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
```

**Practice Exercises**

1. How would you return the days from Friday to Sunday?
2. How would you get all the weekdays?
3. What about the weekend?

#### Max and Min

One other useful thing you can do with lists is to find the max an min of the values inside of the lists. Depending on the type of data inside of the list this  might look a little different. Go ahead and take the min and max of a these lists following the example here:

```python
my_integers = [0, 1, 2, 3, 4, 5, 6]
min(my_integers)
max(my_integers)
my_numbers = [0, 1.6, 1.3, 6.9, 1, 7, 16]
alpha_numeric = ["1a", "2b", "a4", "z5", "z", "a"]
days = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
string_numbers = ["1", "2", "11", "22", "3"]
```

As you can start to tell, min and max work differently on strings and numbers. The numbers (both floats and integers) give the results you would expect with the biggest or smallest numerical values coming back. Strings are sorted alphabetically and the first value is the min with the last value as the max.

#### Lists and Variables

Try this:

```python
a = [1, 2, 3]
b = a
c = a[:]
a.append(4)
```

Now take a look at `a`, `b`, and `c`. Notice how `c` was a *copy* of `a`. Contrastingly, `b` is the *same list* `a`. Essentially, this is demonstration of how variables aren't the values themselves. They are merely pointing to the values. In this case, `b` and `a` both point to the same list on your computer, and when you modify either one you're actually modifying the same list behind the scenes.

### Tuples

Tuples are a similar concept to lists. You create them with parentheses instead of square brackets and you access them the same way as you do lists. The main distinction is that you cannot modify them the same way you can with lists.

```python
my_tuple = (1, 2, "My Computer")
my_tuple[2]
```

But if you try to `my_tuple.append(4)` you'll see a Traceback error:

```
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'tuple' object has no attribute 'append'
```

This error is basically letting you know that you can't append to tuples! You also can't insert, pop, remove, or modify them in any way!  

## [Next... Part 8](part8.md)

### [Previous... Part 6](part6.md)