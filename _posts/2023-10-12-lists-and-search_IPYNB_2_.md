---
layout: post
title: Linux Shell and Bash
description: A Tech Talk on Linux and the Bash shell.
toc: True
comments: True
courses: {'compsci': {'week': 9}}
type: tangibles
---

# Made by: Ryan, Daniel, Saaras, Will, and Andrew

## Python lists Operations

### Append function
# From the Data Abstractions Unit we Learned about lists and how they can store multiple variables 
# Today we're going to show you how to add items to lists utilizing the append option


```python

lst = ["hi"]
lst.append("no")
print(lst)
```

    ['hi', 'no']


### Insert function
- The insert function allows you to append items to different lists at a specific location.
- Let's first understand how it may work through pseudocode

#### Exmaple 1
INSERT alist, pos, value 
INSERT alist, 1, "hi" 
- Here the alist represents your list you want to append an item to
- The position is where on the list the item will be generated in respect to the current list
- Finally, the value is the item you're adding to your list. 
- So in the code provided below, in position 1 you insert the item "hi" into alist

### Your turn!!!!
- Turn this pseudocode into python
- How may we want to implement this on python? Think back to the data abstraction unit. 
- ( Hint: Think about the differences between psueodcode and python )


```python
# ANSWER: 
lst = ["hi"]
lst.append("no") 
# Inserting items to a specific list, remember python is 0 based on the items!!
lst.insert(5, " maybe")
print(lst)
```

    ['hi', 'no', ' maybe']


### Remove function
- The remove functions allows you to remove specific items at a specific position on the list

#### Pseudocode example
- REMOVE aList, pos




```python
lst = ["hi", "bye"]
lst.remove(lst[0])
print(lst)
## You can also access the list by the position, this is called list indexing
print(lst[0])
```

    ['bye']
    bye


### Let's do some Collegeboard exercises
- In the following list:
  - nums = [65, 89, 92, 35, 84, 78, 28, 75]
- Figure out what the minimum number in the list, WITHOUT using the other methods and premade functions.

### Second question:
- Let's say we have a list called "animals" from a survey that stores whether or not they prefer "cats" or "dogs" as strings in this list.
- Transverse this list and tell me the total amount cats and dogs in the list



```python
nums = [65, 89, 92, 35, 84, 78, 28, 75]
print(nums[3])
print("this number is the lowest number in the nums list")
## Your code here
```

    35
    this number is the lowest number in the nums list



```python
animals = ["cats", "dogs"]

animals.remove("dogs")
print(animals)
print("only one person works at this petshop and she likes cats.")
```

    ['cats']
    only one person works at this petshop and she likes cats.


### ITS BINARY SEARCH TIME
- By the end of this you should be able to know what binary search is
- What the time complexity of binary search is
- How to derive the time complexity for binary search

### HOW DOES BINARY SEARCH WORK
- pay attention to the demonstration in the front
- volunteers will be called up
- candy if you participate

Binary search is like a guessing game where you halve your options at each step. Imagine you're finding a name in a phone book:

1. **First Step:** You open the book in the middle.
2. **Second Step:** Is the name before or after the middle? You eliminate half of the remaining names.
3. **Repeat:** Keep dividing until you find the name or run out of names to check.
4. **MAKE SURE YOUR LIST IS SORTED** Binary search will not work if the list isn't sorted

Because you're halving the options each time, it's super quick. If you have \(n\) names, it takes at most \( \log_2(n) \) steps to find a name. This efficiency, where the time it takes doesn't increase much as the number of names in the phone book grows, is what makes binary search awesome! Binary search is also more optimal for searcihng compared to a linear search for anything that doesnt include small lists..


### Demo Being shown above
The sorted list we have currently, has integers [1, 3, 4, 5, 13, 20], we are currently trying to find the index of the the integer 1 within the list

How it works is we start at element 0 for our left position and element 5 for our rightwards position

Our middle position becaomes 5 because ((5+0)//2)=3 so element 3

Our element 3 within the list gives us the integer 5

We then realize that oh 5 is greater then 3 so we have to move leftwards

Then to make the algorithm more efficient we move the r backwards 1 beacuse we have already checked at this point

So now we can reduce the list to [1, 3, 4]

Now we can repeat the same steps as before and find the middle of this list which is 3

We realize thats not equivalent to the integer 1, and our value is still too great

So we move the middle leftwards 1 positioon

AND BAM THATS HOW YOU CAN DO BINARY SEARCH





```python
#example of binary search in python has a time complexity of O(n)
def binarySearch(arr, x):
    l= 0 #our minimum element
    r=len(arr) - 1 # our maximum element
    while l <= r:
        mid = l + (r - l) // 2 
        if arr[mid] == x:
            return mid
        elif arr[mid] < x:
            l = mid + 1
        else:
            r = mid - 1
    return -1


sorted_list = [2, 5, 8, 12, 16]
target = 3
result = binarySearch(sorted_list, 5)
print(result)

```

    1



```python
#Linear Search Approach in O(n)
def linear_search(target, sorted_list):
    for o in range(len(sorted_list)):
        if sorted_list[o]==target:
            return(o)
#Does not have to be a sorted list for the sake of comparison I just made it sorted
sorted_list = [1, 3, 5, 7, 9, 11, 13, 15]
target = 3
result = linear_search(target, sorted_list)
print(result)

```

    1


Using linear search make a list with elements ["eggs", "milk", "butter", "cake"]
Then randomize an element 1-4 within that list and find the index of it via linear search


```python
#code here

import random


items = ["eggs", "milk", "butter", "cake"]


random_index = random.randint(0, len(items) - 1)
random_item = items[random_index]


def linear_search(target, lst):
    for index, item in enumerate(lst):
        if item == target:
            return index
    return -1 

index = linear_search(random_item, items)


print("List of items:", items)
print(f"Random item: {random_item}")
if index != -1:
    print(f"Index of the random item '{random_item}': {index}")
else:
    print(f"The random item '{random_item}' was not found in the list.")
```

    List of items: ['eggs', 'milk', 'butter', 'cake']
    Random item: cake
    Index of the random item 'cake': 3


How big O Notation works in the context works in the case of search methods.

Lets first explain for linear search, because linear search only requires a iterative approach all we use is O(n), this is due
to the loop infinitely going until it finds the element and then after that it doesnt do anything.

However binary search is special in this sense because you don't actually have to go through an entire loop how you can picture this is by imagining a list with 1000000 integer values in it and my target value is 59223, binary search makes it so that you just divide the list by 2 until you find the element. It's a lot faster then the iterative approach, where I keep going until I get to 59223 what this does is it allows me to speed up the time and memory usage I take. because I keep dividing the list by 2 allowing for me to form a logarithm because its just repetitive multiplication of 1/2 and then that makes it so that O(log(n)) becomes the time complexity for the Binary search algorithm.




HW TIME!!!!!!!!!!!!!!!!!!
We want you guys to make a guessing game below, where utilizing binary search you can within a list of 100 sorted elemments find, a value that your code will randomize using random.randint(). We want you to also make it so every iteration output the number is higher up or lower until you actually get to the answer. We also want number of tries it took to guess the number. Points will be awarded for customizations and potential changes.

Extra credit (for above 95%): Send a screenshot on me to slack showing you can do this: https://codeforces.com/contest/1201/problem/C


```python
#Code in here

import random

sorted_list = list(range(1, 101))

target_number = random.randint(1, 100)

def binary_search_guessing_game(sorted_list, target_number):
    low = 0
    high = len(sorted_list) - 1
    tries = 0
    
    while low <= high:
        mid = (low + high) // 2
        guess = sorted_list[mid]
        
        print(f"Guess #{tries + 1}: {guess}")
        
        if guess == target_number:
            print(f"Congratulations! The target number {target_number} was found in {tries + 1} tries.")
            break
        elif guess < target_number:
            low = mid + 1
            print("The target number is higher.")
        else:
            high = mid - 1
            print("The target number is lower.")
        
        tries += 1


print(f"Try to guess the target number between 1 and 100.")
binary_search_guessing_game(sorted_list, target_number)

```

    Try to guess the target number between 1 and 100.
    Guess #1: 50
    The target number is higher.
    Guess #2: 75
    The target number is lower.
    Guess #3: 62
    The target number is lower.
    Guess #4: 56
    The target number is higher.
    Guess #5: 59
    Congratulations! The target number 59 was found in 5 tries.


HW Part 2: This time instead of utilizing binary search to do it I want you to use linear search to get to the same value and I want you to output the number of iterations it took to get there. Aswell as a congrats message upon getting there points will be awarded upon creativity and completion.


```python
#Code in here

import random

# Generate a sorted list of 100 elements
sorted_list = list(range(1, 101))

# Generate a random target number
target_number = random.randint(1, 100)

def linear_search_guessing_game(sorted_list, target_number):
    tries = 0
    
    for guess in sorted_list:
        tries += 1
        print(f"Guess #{tries}: {guess}")
        
        if guess == target_number:
            print(f"Congratulations! The target number {target_number} was found in {tries} tries.")
            break

# Start the game
print(f"Try to guess the target number between 1 and 100.")
linear_search_guessing_game(sorted_list, target_number)

```

    Try to guess the target number between 1 and 100.
    Guess #1: 1
    Guess #2: 2
    Guess #3: 3
    Guess #4: 4
    Guess #5: 5
    Guess #6: 6
    Guess #7: 7
    Guess #8: 8
    Guess #9: 9
    Guess #10: 10
    Guess #11: 11
    Guess #12: 12
    Guess #13: 13
    Guess #14: 14
    Guess #15: 15
    Guess #16: 16
    Guess #17: 17
    Guess #18: 18
    Guess #19: 19
    Guess #20: 20
    Guess #21: 21
    Guess #22: 22
    Guess #23: 23
    Guess #24: 24
    Guess #25: 25
    Guess #26: 26
    Guess #27: 27
    Guess #28: 28
    Guess #29: 29
    Guess #30: 30
    Guess #31: 31
    Guess #32: 32
    Guess #33: 33
    Guess #34: 34
    Guess #35: 35
    Guess #36: 36
    Guess #37: 37
    Guess #38: 38
    Guess #39: 39
    Guess #40: 40
    Guess #41: 41
    Guess #42: 42
    Guess #43: 43
    Guess #44: 44
    Guess #45: 45
    Guess #46: 46
    Guess #47: 47
    Guess #48: 48
    Guess #49: 49
    Guess #50: 50
    Guess #51: 51
    Guess #52: 52
    Guess #53: 53
    Guess #54: 54
    Guess #55: 55
    Guess #56: 56
    Guess #57: 57
    Guess #58: 58
    Guess #59: 59
    Guess #60: 60
    Guess #61: 61
    Guess #62: 62
    Guess #63: 63
    Guess #64: 64
    Guess #65: 65
    Guess #66: 66
    Guess #67: 67
    Guess #68: 68
    Guess #69: 69
    Congratulations! The target number 69 was found in 69 tries.

