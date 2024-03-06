# What is map?

In Python, the map() function is used to apply a function to all the items in an iterable (like a list, tuple, or dictionary) and returns an iterator that yields the results.

##### Example

```python
# Define a function
def square(x):
    return x * x

# Define a list
numbers = [1, 2, 3, 4, 5]

# Use map to apply the function to each item in the list
squared_numbers = map(square, numbers)

# Convert the result to a list (or iterate over it)
squared_numbers_list = list(squared_numbers)

print(squared_numbers_list)  # Output: [1, 4, 9, 16, 25]
```

We can also use lambda functions with map function to make the code more concise:

```python
# Define a list
numbers = [1, 2, 3, 4, 5]

# Use map to apply the function to each item in the list
squared_numbers = map(lambda x: x * x, numbers)

# Convert the result to a list (or iterate over it)
squared_numbers_list = list(squared_numbers)

print(squared_numbers_list)  # Output: [1, 4, 9, 16, 25]
```
