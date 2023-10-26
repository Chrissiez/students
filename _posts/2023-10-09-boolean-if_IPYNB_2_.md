---
toc: False
comments: False
layout: post
title: Boolean, If Lesson
description: Team LEIA
type: hacks
courses: {'compsci': {'week': 8}}
---

# Boolean

- A Boolean value is either true or false.
- A Boolean expression produces a Boolean value (true or false) when evaluated.

## <mark>Conditional ("if") statements</mark>

- Affect the sequential flow of control by executing different statements based on the value of a Boolean expression.


```python
IF (condition)
{
	<block of statements>
}

The code in <block of statements> is executed if the Boolean expression condition evaluates to true; no action is taken if condition evaluates to false.

IF (condition)
{
	<block of statements>
}
ELSE
{
	<second block of statements>
}

The code in the first <block of statements> is executed if the Boolean expression condition evaluates to true; otherwise, the code in <second block of statements> is executed.
```

<b>Example:</b> Calculate the sum of 2 numbers. If the sum is greater than 10, display 10; otherwise, display the sum.


```python
num1 = INPUT
num2 = INPUT
sum = num1 + num2
IF (sum > 10)
{
	DISPLAY (10)
}
ELSE
{
	DISPLAY (sum)
}
```

# Hack 1

- Add a variable that represents an age.

- Add an 'if' and 'print' function that says "You are an adult" if your age is greater than or equal to 18.

- Make a function that prints "You are a minor" with the else function.


```python
## YOUR CODE HERE

age = input("what is your age?")

if int(age) >= 18:
    print ("You are an adult")
else:
    print ("You are a minor")
```

    You are a minor


## <mark><b>Relational operators:</b></mark> 
- Used to test the relationship between 2 variables, expressions, or values. These relational operators are used for comparisons and they evaluate to a Boolean value (true or false).

<b>Ex.</b> a == b evaluates to true if a and b are equal, otherwise evaluates to false

- a == b (equals)	
- a != b (not equal to)
- a > b (greater than)
- a < b (less than)
- a >= b (greater than or equal to)
- a <= b (less than or equal to)

<b>Example:</b> The legal age to work in California is 14 years old. How would we write a Boolean expression to check if someone is at least 14 years old?

age >= 14

<b>Example:</b> Write a Boolean expression to check if the average of height1, height2, and height3 is at least 65 inches.

(height1 + height2 + height3) / 3 >= 65

# Hack 2

- Make a variable called 'is_raining' and set it to 'True".

- Make an if statement that prints "Bring an umbrella!" if it is true

- Make an else statement that says "The weather is clear".


```python
## YOUR CODE HERE

is_raining = True

if is_raining == True:
    print("Bring an umbrella!")
else:
    print("The weather is clear")
```

    Bring an umbrella!


## <mark><b>Logical operators:</b></mark>
Used to evaluate multiple conditions to produce a single Boolean value.

- <b>NOT</b>	evaluates to true if condition is false, otherwise evaluates to false
- <b>AND</b>	evaluates to true if both conditions are true, otherwise evaluates to false
- <b>OR</b>	evaluates to true if either condition is true or if both conditions are true, otherwise evaluates to false

<b>Example:</b> You win the game if you score at least 10 points and have 5 lives left or if you score at least 50 points and have more than 0 lives left. Write the Boolean expression for this scenario.

(score >= 10 AND lives == 5) OR (score == 50 AND lives > 0)

## <mark><b>Relational and logical operators:</b></mark>

<b>Example:</b> These expressions are all different but will produce the same result.

- age >= 16
- age > 16 OR age == 16
- NOT age < 16

# Hack 3

- Make a function to randomize numbers between 0 and 100 to be assigned to variables a and b using random.randint

- Print the values of the variables

- Print the relationship of the variables; a is more than, same as, or less than b


```python
## YOUR CODE HERE

import random

a = random.randint(0,100)
b = random.randint(0,100)

print("a = " + str(a))
print("b = " + str (b))

if a > b:
    print("a is more than b")
elif a == b:
    print("a is the same as b")
else:
    print("a is less than b")
```

    a = 34
    b = 89
    a is less than b


## <b>Homework</b>

### Criteria for above 90%:
- Add more questions relating to Boolean rather than only one per topic (ideas: expand on conditional statements, relational/logical operators)
- Add a way to organize the user scores (possibly some kind of leaderboard, keep track of high score vs. current score, etc. Get creative!)
- Remember to test your code to make sure it functions correctly.


```python
#HOMEWORK


# The quiz contains questions related to Boolean values, Boolean expressions,
# conditional statements, relational operators, and logical operators.

# Import necessary modules
import getpass  # Module to get the user's name
import sys  # Module to access system-related information

# Function to ask a question and get a response
def question_with_response(prompt, answer, correct):
    # Print the question
    print(prompt)
    # Get user input as the response
    msg = input()
    if msg == answer:
        correct = True
        print("That's correct")
        return True
    else:
        print("Incorrect")
        return False

# Define the number of questions and initialize the correct answers counter
questions = 15
correct = 0

# Personalized greeting message
# Collect the student's name
user_name = input("Enter your name: ")
print('Hello, ' + user_name + " running " + sys.executable)
print("You will be asked " + str(questions) + " questions.")
answer = input("Are you ready to take a test?")

if answer == ("yes"):
    print("Let's Begin!")

    # Question 1: Boolean Basics 
    # Ask a question about Boolean values and check the response
    # Provide feedback based on the correctness of the response
    question_with_response("What statement is used to evaluate booleans?", "if else", correct)

    # Question 2: Boolean Expressions
    # Ask a question about Boolean expressions and their importance in programming
    # Provide feedback based on the correctness of the response
    question_with_response("Why are booleans important?", "evaluate values", correct)


    # Question 3: Conditional Statements
    # Ask a question about the purpose of conditional (if-else) statements in programming
    # Provide feedback based on the correctness of the response
    question_with_response("What is conditional for?", "control flow", correct)


    # Question 4: Relational Operators
    # Ask a question about common relational operators in programming and provide examples
    # Provide feedback based on the correctness of the response
    question_with_response("What is a common relational operator?", "!=", correct)


    # Question 5: Logical Operators
    # Ask a question about the use of logical operators in programming and provide examples
    # Provide feedback based on the correctness of the response
    question_with_response("What is the use of logical operators?", "connect expressions", correct)

    # Question 6: Boolean Logic
    # Ask a question about basic Boolean logic
    # Provide feedback based on the correctness of the response
    question_with_response("What is the result of 'True and True'?", "True", correct)

    # Question 7: Boolean Values
    # Ask a question about the possible values of a Boolean variable
    # Provide feedback based on the correctness of the response
    question_with_response("What are the possible values of a Boolean variable?", "True or False", correct)

    # Question 8: if-else Statements
    # Ask a question about the syntax of an if-else statement
    # Provide feedback based on the correctness of the response
    question_with_response("What is the syntax of an 'if-else' statement in Python?", "if condition: \n    # code block\nelse:\n    # code block", correct)

    # Question 9: Conditional Statements
    question_with_response("What is the purpose of an 'if' statement?", "Conditional execution", correct)

    # Question 10: Relational Operators
    question_with_response("What does '==' mean in Python?", "Equal to", correct)

    # Question 11: Logical Operators
    question_with_response("What is the result of 'True and False'?", "False", correct)

    # Question 12: Boolean Data Type
    question_with_response("In Python, what data type represents Boolean values?", "bool", correct)

    # Question 13: Logical NOT
    question_with_response("What is the result of 'not True'?", "False", correct)

    # Question 14: Boolean Conversion
    question_with_response("How can you convert a non-Boolean value to a Boolean in Python?", "bool() function", correct)

    # Question 15: Combining Logical Operators
    question_with_response("What is the result of 'True or (False and True)'?", "True", correct)

    # Display the final score
    # Calculate the percentage of correct answers and provide feedback
    print(user_name + ", you scored " + str(correct) + "/" + str(questions))
else: 
    print("Ok, Have a good day.")

```

    Hello, chrissie running /bin/python
    You will be asked 15 questions.
    Let's Begin!
    What statement is used to evaluate booleans?
    Incorrect
    Why are booleans important?
    Incorrect
    What is conditional for?
    Incorrect
    What is a common relational operator?
    Incorrect
    What is the use of logical operators?
    Incorrect
    What is the result of 'True and True'?
    Incorrect
    What are the possible values of a Boolean variable?
    Incorrect
    What is the syntax of an 'if-else' statement in Python?
    Incorrect
    What is the purpose of an 'if' statement?
    Incorrect
    What does '==' mean in Python?
    Incorrect
    What is the result of 'True and False'?
    Incorrect
    In Python, what data type represents Boolean values?
    Incorrect
    What is the result of 'not True'?
    Incorrect
    How can you convert a non-Boolean value to a Boolean in Python?
    Incorrect
    What is the result of 'True or (False and True)'?
    Incorrect
    chrissie, you scored 0/15

