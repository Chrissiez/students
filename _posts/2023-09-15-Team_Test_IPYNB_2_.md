---
toc: True
comments: False
layout: post
title: Team Test
type: hacks
courses: {'csp': {'week': 4}}
---

<hr style="solid">

### Program with Output
- Include a code example that demonstrates a simple program with an output.


```python
print("Hello, world!")
```

<hr style="solid">

### Program with Input / Output
- Show a program that takes user input and produces output.


```python
name = input("Enter your name: ") 
print ("Hello, " + name + "!") 
```

<hr style="solid">

### Program with a List
- Demonstrate a program that uses a list.


```python
fruits = ["apple", "banana", "cherry"] 
for fruit in fruits: print(fruit) 
```

<hr style="solid">

### Program with a Dictionary
- Showcase a program utilizing a dictionary.


```python
person = {"name": "John", "age": 30, "city": "New York"} 
print(person["name"]) 
```

<hr style="solid">

### Program with Iteration
- Provide an example of a program that uses iteration (e.g., a for loop).


```python
for i in range(5): 
    print(i) 
```

<hr style="solid">

### Program with a Function
- Create a function that performs a mathematical or statistical calculation.


```python
def calculate_average(numbers): 
    total = sum(numbers) 
    return total / len(numbers)
numbers = [10, 20, 30, 40, 50] 
average = calculate_average(numbers) 
print("Average:", average) 
```

<hr style="solid">

### Program with a Selection/Condition
- Include a program with a selection or condition (e.g., if/else statement).


```python
x = 10 
if x > 5: 
    print("x is greater than 5") 
else: 
    print("x is not greater than 5") 
```

<hr style="solid">

### Debugging
- Explain the overall purpose of this program, summarizing what you've covered.


```python
# Initial version with an error
x = 10
y = 0
try:
    result = x / y
except ZeroDivisionError as e:
    print("Error:", e)

# Debugging steps to fix the error
try:
    if y == 0:
        raise ValueError("y cannot be zero")
    result = x / y
except ValueError as e:
    print("Error:", e)


# Corrected version
def divide(x, y):
    if y == 0:
        raise ValueError("y cannot be zero")
    return x / y
try:
    result = divide(x, y)
except ValueError as e:
    print("Error:", e)
else:
    print("Result:", result)
```


```python
# Debugging steps to fix the error 
try: 
    if y == 0: 
        raise ValueError("y cannot be zero") 
    result = x / y 
except ValueError as e: 
    print("Error:", e) 
```

The code block above demonstrates the steps to fix the error by checking for a zero division condition and raising a ``ValueError`` with a meaningful error message.


```python
# Corrected version:
def divide(x, y): 
    if y == 0: 
        raise ValueError("y cannot be zero") 
    return x / y 
try: 
    result = divide(x, y) 
except ValueError as e: 
    print("Error:", e) 
else: 
    print("Result:", result) 
```

The code block above provides the corrected version of the code using a ``divide`` function that includes the fix. It also includes error handling to catch and handle any exceptions, and it prints the result if there are no errors.







<hr style="solid">

### Program with Purpose
- Explain the overall purpose of this program, summarizing what you've covered.

<hr style="solid">

### Conclusion
- Provide a concluding statement, summarizing the key concepts and skills learned in the notebook.
