# A Complete Beginner's Introduction to Python

## Part 9

### Dictionaries

A dictionary is another way to store data in Python. Dictionaries have `keys` and `values`. To create a dictionary you use the curly braces syntax `{}`.

Here's how we create a dictionary with a few values and assign it to the variable `names_and_numbers`:

```python
names_and_numbers = {
    'Fernando': 'Ok',
    'Prince': 'Amazing',
    'The Artist Formerly Known as Prince': 'Awesome',
    2: "Hello",
    "Goodbye": 12.6,
}
```

We can reference dictionaries in a similar way to how we reference tuples and lists. With those, we referenced the position in the list or tuple. In this case, we can reference the *key*.

For example, `names_and_numbers['Fernando']` would give us the string: `'Ok'`. And if we used the key of `2`, we get `'Hello'`, not `'Prince'` or `'Amazing'`.

But we don't have to start knowing what everything inside our dictionary will be. We can start an empty dictionary and go from there:

```python
friends_numbers = {}

friends_numbers["James"] = "333-666-8999"
friends_numbers["Hugo"] = "555-111-3232"
print(friends_numbers)
friends_numbers["Che"] = "777-222-4545"
print(friends_numbers)
```

#### pop and Dictionaries

Similarly to lists, you can `pop` elements off the dictionary:

```python
friends_numbers.pop("James")
```

This will return James' number and remove him and his number from the dictionary.

#### Dictionary `keys()` and `values()`

You can also get all the keys from a dictionary by adding `.keys()` to the end or all the values by adding a `.values()`. Both of these will return an object that you can iterate over but that you can't manipulate in the same way as a list unless you explicitly change it into one with `list()`.

```python
friends_numbers.keys()

result = friends_numbers.values()
result[0] # This will fail
new_result = list(result)
new_result[0] # This will work!
```

## [PNext... Part 10](part10.md)

### [Previous... Part 8](part8.md)