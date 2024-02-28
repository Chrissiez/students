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

## 11. Color represented by binary triplet

A color in a computing application is represented by an RGB triplet that describes the amount of red, green, and blue, respectively, used to create the desired color. A selection of colors and their corresponding RGB triplets are shown in the following table. Each value is represented in decimal (base 10).

|Color Name|RGB Triplet|
|-|-|
|indigo	| (75,   0, 130)|
|ivory|	(255, 255, 240)|
|light pink|	(255, 182, 193)​|
|light yellow|	(255, 255, 224)|
|magenta|	(255,   0, 255)|
|neutral gray|	(127, 127, 112)|
|pale yellow|	(255, 255, 160)|
|vivid yellow|	(255, 255,  14)|

According to information in the table, what color is represented by the binary RGB triplet (11111111, 11111111, 11110000)?

A. Ivory
B. Light Yellow
C. Neutral Gray
D. Vivid Yellow

### Correct Answer: A

The binary number 11111111 is equal to 2^7 + 2^6 + 2^5 + 2^4 + 2^3 + 2^2 + 2^1 + 2^0, or 255. The binary number 11110000 is equal to 2^7 + 2^6 + 2^5 + 2^4, or 240. Therefore, the given binary triplet represents the color ivory.

### My Answer: B

The third binary number for light yellow is 11100000 while ivory is 11110000. I must have accidentally forgotten to add 2^4 and got 224 instead of 240


## 23. Flowchart to set available

A flowchart is a way to visually represent an algorithm. The flowchart below is used by an application to set the Boolean variable available to true under certain conditions. The flowchart uses the Boolean variable weekday and the integer variable miles.

|Block|	Explanation|
|-|-|
|Oval	|The start or end of the algorithm|
|Diamond|	A conditional or decision step, where execution proceeds to the side labeled true if the condition is true and to the side labeled false otherwise|
|Rectangle|	One or more processing steps, such as a statement that assigns a value to a variable|

Which of the following statements is equivalent to the algorithm in the flowchart?

A. available <-- weekday or miles < 20

B. available <-- weekday and miles > 20

C. available <-- weekday or miles > 20

D. available <-- weekday and mlies <20

### Correct Answer:D

The flowchart sets available to true whenever weekday is true and miles is less than 20, and sets available to false otherwise. This code statement provides the same functionality.

### My Answer B: 

I must have read the symbol wrong because the flowchart is quite easy to read
