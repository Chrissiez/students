---
toc: True
comments: True
layout: post
title: Tri 2 Individual Review
description: overview of the project
type: hacks
courses: {'compsci': {'week': 10}}
---

# Condensed Project Overview:

We Created a platform to play unblocked games at school. With the school blocking almost every game imaginable, we decided to add a couple of our favorite games to play. We added a login page for users to keep track of their highscores across all of the games.

# My Feature:

My feature was the tetris game that speeds up after completing 10 rows and keeps track of your highest score.



## How it Meets CollegeBoard Requirements

[link to requirements](https://apcentral.collegeboard.org/media/pdf/ap-csp-student-task-directions.pdf)

| College Board Requirement: | What I did: |
|-|-|
|Instructions for input from one of the following: user, a device, an online data steam, or a file | The user clicks any where on the screen to start playing|
|Use of at least one list (or other collection type) to represent a collection of data that is stored and used to manage program complexity and help fulfill the users purpose.| An example of a collection of data that is stored is of the collection high scores from the game. It helps fulfill our program’s purpose because we use the data of all the highscores so users can see how they do. I am storing all collections in and SQLite table and using JSON collection to pass data from frontend to and from the backend|
|At least one procedure that contirubted to the program’s intened purpose where you have defined: the name, return type, one or more parameters:| This procedure has a name(Score), return(self.name) and a parameter(db.Model): ![procedure](<img width="604" alt="call-code" src="https://github.com/Chrissiez/students/assets/142445376/edf7f8a5-1c02-48db-a56c-396a4edffa29">
) |
|An algorithm that includes sequencing, selection, and iteration that is in the body of the selected procedure| This combination of sequencing, selection, and iteration demonstrates a common algorithmic pattern used for processing grids or matrices in various applications. ![sequencing](<img width="325" alt="sequencing" src="https://github.com/Chrissiez/students/assets/142445376/8938fe55-3405-4a0d-8af8-1c51d3510638">)|
|Calls to your student-developed prodcedure:| fetches highscore ![get](<img width="575" alt="fetch-code" src="https://github.com/Chrissiez/students/assets/142445376/b5a128f1-d857-49cd-97e3-3b7e7dd81d96">)|
|Instructions for output (tactile, audible, visual, or ) based on input and program functionality:|This sets up the game after the user starts it ![draw](<img width="381" alt="output-code" src="https://github.com/Chrissiez/students/assets/142445376/ae0d463f-435b-4796-a4a0-5c71358e67c0">)
|


# Video

|Collegboard Requirements	|My Video|
|-|-|
|Input to program|	Seen in video, playing the game|
|At least one aspect of the functionality of your program|	the game displays scoring, lines, and levels during the game and updates highest score after|
|Output produced by program:|	keeps highest score|
|My video does not have:|	any distinguishing information and voice narration|
|My video is|	a .webmb, less than 1 minute in length, less than 30MB in file size|
