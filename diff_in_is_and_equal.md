# What is the difference between is and == in python?

### == (Equality Operator)

The equality operator compares the value or equality of two objects. It checks if the values on both sides are equal. It is used to compare the content or the value of the objects.

#### Example 1

```python
x = [1, 2, 3]
y = [1, 2, 3]

# True, because the content of x and y is the same.
print(x == y)
```

#### Example 2

```python
x = [1, 2, 3]
y = [1, 2, 3]

# False, because x and y refer to different objects in memory.
print(x is y)
```

### is (Identity Operator)

Is operator checks whether two variables refer to the same object in memory.

#### Example 3

```python
x = [1, 2, 3]
# Both x and y now reference the same object in memory
y = x

# True, because x and y refer to the same object
print(x is y)
```
