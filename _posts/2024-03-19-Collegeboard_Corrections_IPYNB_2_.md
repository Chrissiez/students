---
toc: True
comments: True
layout: post
title: College Board Quiz
description: notes about the quiz
type: hacks
courses: {'compsci': {'week': 10}}
---

# Questions I got wrong:

## Q9 Digital representation of audio signal

Which of the following best explains how an analog audio signal is typically represented by a computer?

A) An analog audio signal is measured as input parameters to a program or procedure. The inputs are represented at the lowest level as a collection of variables.
B) An analog audio signal is measured at regular intervals. Each measurement is stored as a sample, which is represented at the lowest level as a sequence of bits.
C) An analog audio signal is measured as a sequence of operations that describe how the sound can be reproduced. The operations are represented at the lowest level as programming instructions.
D) An analog audio signal is measured as text that describes the attributes of the sound. The text is represented at the lowest level as a string.


### Correct Answer: B

Analog signals are sampled digitally at discrete intervals over time. These samples, like all digital data, are represented at the lowest level as a sequence of bits.

### What I answered: A 

While some programs or procedures take audio data as input, this is not how audio data are represented digitally. At the lowest level, all digital data are represented as sequences of bits

## Q55 Move element from end of list to beginning

A code segment is intended to transform the list utensils so that the last element of the list is moved to the beginning of the list.
For example, if utensils initially contains ["fork", "spoon", "tongs", "spatula", "whisk"], it should contain ["whisk", "fork", "spoon", "tongs", "spatula"] after executing the code segment.
Which of the following code segments transforms the list as intended?

### Correct Answer: C

len 
 LENGTH(utensils)

temp 
 utensils[len]

REMOVE(utensils, len)

INSERT(utensils, 1, temp)

This code segment assigns the value of the last element of the list to the variable temp, then removes the last element of the list, then inserts temp as the first element of the list.

### My Answer: A

len 
 LENGTH(utensils)

temp 
 utensils[len]

REMOVE(utensils, len)

APPEND(utensils, temp)

This code segment assigns the value of the last element of the list to the variable temp, then removes the last element of the list, then appends temp to the end of the list. The resulting list is the same as the original list.
