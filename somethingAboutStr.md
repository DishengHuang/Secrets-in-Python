# Something about the string

We try to replace the "a" with "1", and remove the white space on the string. However, nothing has changed. This is because strings are immutable in python. We need to reassign the strings for the x.

```python
# Nothing has changed
x = "   abc"
x.replace("a", "1")
x.strip()
print(x) # "   abc"
```

```python
x = " abc"
x = x.replace("a", "1")
x = x.strip()
print(x) # "1bc"
```
