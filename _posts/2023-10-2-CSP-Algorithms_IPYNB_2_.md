---
toc: False
layout: post
title: ALGORITHMS
description: Team SRSC
type: hacks
courses: {'compsci': {'week': 7}}
comments: True
---

# ALGORITHMS 
## SRSC 


# <mark>BIG IDEA: A FINITE SET OF INSTRUCTIONS THAT ACCOMPLISH A SPECIFIC TASK 



## SEQUENCING 

### <mark> DO STEPS OF CODE IN THE ORDER SPECIFIED 

first step -> second step -> third step


```python
number = int(input("Enter a number: "))

result = number * 2
print("double of " + str(number) + " is " + str(result))

```

    double of 1is 2



1. Create a variable based on user input <br>
2. Multiply variable by two<br>
3. Print out both variables at the end<br>



## SELECTION 

### <mark> Choose TWO OR MORE OUTCOMES based on a DECISION or CONDITION 



```python
number = 6
if number % 2 == 0:
    print("Even")
else:
    print("Odd")

```

    Even


1. Set number to 5 <br>
2. If number is divisible by 2 with no remainder, print "Even" <br>
3. Otherwise, print "Odd" <br>


# ITERATION 

## <mark> REPEAT STEPS BASED ON A DECISION or STOP when a condition is met 

first step -> 
second step -> 
if step 2: true -> first step 
if step 2: false -> third step 
-> fourth step 


```python

fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)


```

    apple
    banana
    cherry


1. Create a list called fruits <br>
2. For each fruit in the list, print the fruit


# ACTIVITY 1: Robot Pseudocode 

[Link to Robot Question 2](https://assets.learnosity.com/organisations/537/VR165972.g03.png)

Write the pseudocode to move the robot onto the gray square. 

Available Code: <br>
Move forward <br>
Turn Left <br>
Turn Right <br>





PseudoCode here: <br>
Move forward
Move forward
Move Forward
Turn Left 
Move Foward
Move Forward
Turn Right
Move Forward
Move Forward
Move Forward


```python
# Math Operations:

print("Addition") #addition
result = 5 + 3
print(result)  # 8

print("\nSubtraction") #subtraction
result = 10 - 4
print(result)  # 6

print("\nMultiplication") #multiplication
result = 6 * 7
print(result)  # 42

print("\nFloat Division") #float division (float = numbers with decimal values)
result = 20 / 3
print(result)  # 5.0

print("\nInteger Division (floor division)") #floor division
result = 20 // 3
print(result)  # 5

print("\nModulus (remainder)") #remainder
result = 10 % 3
print(result)  # 1
```

    Addition
    8
    
    Subtraction
    6
    
    Multiplication
    42
    
    Float Division
    6.666666666666667
    
    Integer Division (floor division)
    6
    
    Modulus (remainder)
    1


## Fibonacci 


```python
def fibonacci(n): #fibonacci sequence 
    fib_series = [0, 1]  

    while len(fib_series) < n:
        next_number = fib_series[-1] + fib_series[-2]  
        fib_series.append(next_number)  

    return fib_series

n = 10  
result = fibonacci(n)
print(result)  # [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]

# initial length of list is 2 
# while length of list is less than amount of numbers we want in our final sequence
# add the last two numbers of the list 
# add this value to the end of the list 
# repeat until length of list reaches n

```

    [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]


## Mini Lesson: If, Else Statements


```python
num =0

if num > 0:
    print(str(num) + " is positive.")
elif num < 0:
    print(str(num) + " is negative.")
else:
    print(str(num) + " is zero.")

```

    0 is zero.


## Mini Lesson 2: For, While Loops


```python
names = ["Alice", "Bob", "Charlie", "David", "Eve"]
for name in names:
    print(name)


num = 1
while num <= 5:
    print(num)
    num += 1

```

    Alice
    Bob
    Charlie
    David
    Eve
    1
    2
    3
    4
    5


## Mini Lesson 3: Defining Function 


```python

def calculate_square(number):
    square = number * number
    return square #ends function 

result = calculate_square(5)
print(f"The square of 5 is {result}")

```

## Mini Lesson 4: Input


```python
variable1 = input("How old are you?")
print("You are " + variable1 + " years old")
```

    You are asd years old


# ACTIVITY 2: CALCULATOR 
1. Create calculator function <br>
2. Allow user to Choose 2 numbers and an operator <br>
3. Perform specified operation based on input <br>
4. Return result of calculation <br>



```python
##YOUR WORK HERE 
##Hint: Use if else statements, defining functions, input

number1 = input("Choose a number.")
symbol = input ("choose an operator.")
number2 = input ("choose another number.")

if symbol == "+":
    print (int(number1) + int(number2))
elif symbol == "-":
    print (int(number1) - int(number2))
elif symbol == "/":
    print (int(number1) / int(number2))
elif symbol == "*":
    print (int(number1)*int(number2))
else:
    print("choose a different operation")

```

    12



```python
# String Operations and Concatenation:

print("\nString Concatenation") #add together strings
str1 = "Hello"
str2 = "World"
result = str1 + " " + str2
print(result)  # "Hello World"

print("\nString Length") #length of string
text = "This is a sample text."
length = len(text)
print(length)  # 22

print("\nString Indexing and Slicing") #string slicing 
text = "Python"
first_char = text[0]
substring = text[2:5]
print(first_char)  # 'P'
print(substring)  # 'tho'


print("\nString Repetition (Repeating Strings)")
text = "Repeat "
result = text * 3
print(result)  # "Repeat Repeat Repeat "

# Palindrome Check Algorithm:

print("\nPalindrome Check Algorithm")

def is_palindrome(text):
    text = text.replace(" ", "").lower()
    return text == text[::-1] ## == will return boolean 

result1 = is_palindrome("racecar")
result2 = is_palindrome("Hello, World!")

print(result1)  # True
print(result2)  # False
```

    
    String Concatenation
    Hello World
    
    String Length
    22
    
    String Indexing and Slicing
    P
    tho
    
    String Repetition (Repeating Strings)
    Repeat Repeat Repeat 
    
    Palindrome Check Algorithm
    True
    False


# ACTIVITY 3: COUNTING VOWELS
1. Create a function that takes a word as an input <br>
2. Use a for loop to iterate through each character of a word <br>
3. Check how many characters in a word contain vowels <br>
4. Return vowel number <br>


```python
##YOUR WORK HERE
```

# <mark> HOMEWORK 
## CREATE TEXT (string) ANALYZER: <br>
### criteria: <br>
1. Accepts input from user <br>
2. Counts total letters, numbers, spaces in a string <br>
3. Counts number of vowels <br>
4. Calculates average word length <br>
5. Correctly displays: total # of characters (including spaces + numbers), total vowels, average word length <br>
### other criteria: <br>
1. ensure that program handles upper and lowercase spelling <br>
2. Test multiple inputs to ensure accuracy 
### Criteria for above 90%: <br>
1. Add a unique program, function, or feature not specified by criterias


### HW Code


```python

def text_analyzer(text):
    # Convert the input text to lowercase for case-insensitive analysis
    text = text.lower()

    # Initialize counters
    total_letters = 0
    total_numbers = 0
    total_spaces = 0
    total_vowels = 0
    total_consonants = 0
    word_count = 0
    word_length_total = 0

    # Define a set of vowels for vowel checking
    vowels = set("aeiou")

    # Define a set of consonants for consonants checking (EXTRA FUNCTION)

    consonants = set("bcdfghjklmnpqrstvwxyz")

    # Iterate through each character in the text
    for char in text:
        if char.isalpha():
            total_letters += 1
            if char in vowels:
                total_vowels += 1
            elif char in consonants:
                total_consonants += 1
        elif char.isdigit():
            total_numbers += 1
        elif char.isspace():
            total_spaces += 1

    # Split the text into words and calculate average word length
    words = text.split()
    for word in words:
        word_count += 1
        word_length_total += len(word)



    # Calculate average word length
    average_word_length = word_length_total / word_count if word_count > 0 else 0

    # Calculate total characters (including spaces and numbers)
    total_characters = total_letters + total_numbers + total_spaces

    # Display the results
    print("Input Text: " + user_input)
    print("Text Analysis Results:")
    print(f"Total # of Characters (including spaces + numbers): {total_characters}")
    print(f"Total Vowels: {total_vowels}")
    print(f"Total Consonants: {total_consonants}")
    print(f"Average Word Length: {average_word_length:.2f}")
    



# Input from the user
user_input = input("Enter a text for analysis: ")
text_analyzer(user_input)
```

    Input Text: AP Chem Sucks
    Text Analysis Results:
    Total # of Characters (including spaces + numbers): 13
    Total Vowels: 3
    Total Consonants: 8
    Average Word Length: 3.67

