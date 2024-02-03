# What is lambda?

In python, lambda function is often used for short-term operations where a full function definition is not necessary. Lambda functions offer several benefits. Here are the examples of the benefits.

#### Conciseness

Lambda functions allow you to write concise and compact code. In the example below, opting for a regular function might require composing three lines of code, whereas achieving an equivalent result with a lambda function can be accomplished in just one line.

##### Example 1

```python
#Regular function (3 lines including the print function)
def add(x, y):
    return x + y
# Output: 8
print(add(3, 5))

#Lambda (1 line)
# Output: 8
print((lambda x, y: x + y)(3, 5))
```

#### Anonymous Functions

From above example (Example 1), Lambda functions are anonymous, and they don't need a name.

#### Convenient for Higher-Order Functions

Lambda functions are commonly used with higher-order functions like map(), filter(), and sorted(). These functions expect a function as an argument, and lambda provides a quick way to create one without defining a separate function. Please check below example 2.

##### Example 2

```python
# List of numbers
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]

# Using a regular function to filter even numbers
def is_even(x):
    return x % 2 == 0

even_numbers_regular = list(filter(is_even, numbers))

# Using a lambda function with filter to achieve the same result
even_numbers_lambda = list(filter(lambda x: x % 2 == 0, numbers))

print(even_numbers_regular)  # Output: [2, 4, 6, 8]
print(even_numbers_lambda)   # Output: [2, 4, 6, 8]
```

# More examples about using the lambda?

##### Example 1

Sort the list by the second item of the elements.

```python
fruits = [(1, "banana"), (2, "apple"), (4, "cherry"), (3, "berry")]

sorted_fruits = sorted(fruits, key = lambda x:x[1])

print(sorted_fruits)
```

##### Example 2

multiply 2 in the list.

```python
fruits = [(1, "banana"), (2, "apple"), (4, "cherry"), (3, "berry")]

double_fruits = map(lambda x:(x[0]*2, x[1]), fruits)

print(double_fruits)
```

# Some drawbrack about using lambda

In the following example, three primary drawbacks of using lambda functions become evident:

1. Single-Line Limitation:
   The lambda function restricts you to expressing your logic within a single line of code.

2. Readability Challenges with Complex Logic:
   When tackling intricate logic, the lambda function's single-line restriction may hinder readability. Crafting comprehensive and clear expressions becomes challenging, potentially leading to code that is difficult for others to understand.

3. Testing and Debugging Complexity:
   Due to the confined nature of lambda functions to a single line, testing and debugging become more challenging. Identifying and rectifying issues in the code may prove cumbersome, as the limited space for expression may hinder effective troubleshooting.

```python
def y_compare_x(x, y):
    if x < y:
        return "greater"
    if x == y:
        return "equal"
    if x > y:
        return "smaller"

lambda x, y: "greater" if x < y else "equal" if x == y else "smaller" if x > y
```
