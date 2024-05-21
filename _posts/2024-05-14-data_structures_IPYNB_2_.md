---
toc: True
comments: True
layout: post
title: Data Structures Write Up
description: write up
type: hacks
courses: {'compsci': {'week': 10}}
---

# Data Structures Write Up

## Collections

<a href="https://ibb.co/mBLNV9s"><img src="https://i.ibb.co/LPLNXxw/squlite.png"></a>

<a href="https://ibb.co/nn6DP9Q"><img src="https://i.ibb.co/3M40R2S/def-init.png"></a>

The first image is of our SQLITE database. The current table in the image is the user database and this holds the user names of people, their real names, DOB, and a hashed password which is used for login and authentication. To create the users, see the second image. Here, we have a python function called initUsers() and this will create all the default users with all of their information.

## Lists and Dictionaries


<a href="https://ibb.co/0hd93N4"><img src="https://i.ibb.co/f4PN7R6/list.png"></a>

This image is from the user query function which will query all the users using a GET request. The return is a list of all the users. But within the list is a dictionary which contains all the user information like name, username, DOB, and more. This is an example of a list and dictionary 1.

## APIs and JSON

<img width="538" alt="postrequest" src="https://github.com/Chrissiez/students/assets/142445376/b7731951-3ad3-451d-9e02-95a47f20a0aa">

![Screenshot 2024-04-17 104706](https://github.com/Chrissiez/students/assets/142445376/bd114e31-b2a6-4532-bfdb-bc0a10000b2d)

<img width="517" alt="putrequestion" src="https://github.com/Chrissiez/students/assets/142445376/da5b3b5e-a88e-407a-8809-229c9ec017cb">

This code show the API code for each request and response using the different methods. The first piece of code is the get request and this will get the users from the database, prepares the output in JSON, and returns it. The post request using self is for reading the user and for creating the user. It sets the UID and sets the email while checking if either field is valid (long enough and that it’s not missing or faked). And then it adds it to the database. This is also an example of data validation because it’s ensuring that the email and username are valid. The update method allows you to add likes or dislikes to the video. It will update the database based on the id type.

## Postman

Post:
<img width="677" alt="postmanpost" src="https://github.com/Chrissiez/students/assets/142445376/78da7a2a-899f-4006-93a0-49c28efd0136">

Get:
<img width="666" alt="postmanget2" src="https://github.com/Chrissiez/students/assets/142445376/6e207418-562c-4061-b370-64545d669f9f">

The first image is a GET request with Postman. This will get all the users. This was used in the user panel/admin panel which displayed all the user information. The second image is a POST request which is for logging in. The body is a JSON payload with the UID (unique to each user) and a password. It will return a JWT token as a sign of authentication

## Frontend

<img width="593" alt="login" src="https://github.com/Chrissiez/students/assets/142445376/cb0cba3b-aff8-452a-923a-9d78145d0c8b">

![Screenshot 2024-04-18 091258](https://github.com/Chrissiez/students/assets/142445376/81a8b876-7009-442c-a7c3-b5e2ab6b4600)

In JavaScript code, describe fetch and method that obtained the Array of JSON objects. In JavaScript code, show code that performs iteration and formatting of data into HTML. In the Chrome browser, show a demo (POST or UPDATE) gathering and sending input and receiving a response that show update. Repeat this demo showing both success and failure. In JavaScript code, show and describe code that handles success. Describe how code shows success to the user in the Chrome Browser screen. In JavaScript code, show and describe code that handles failure. Describe how the code shows failure to the user in the Chrome Browser screen. The code below shows what happens after correctly or incorrectly logging in. If the login is successful, the user will be redirected to the welcome page. If the login fails, an error message will appear on the page.

When I enter the correct username and password (chrissie and 123chris, respectively), I am redirected to the project’s homepage:
<img width="368" alt="successcode" src="https://github.com/Chrissiez/students/assets/142445376/730d3e9a-d711-49b9-a217-9af79550ceb5">
<img width="936" alt="success" src="https://github.com/Chrissiez/students/assets/142445376/ce277a6e-0100-41f5-9c5f-ccfa8ee9526c">


Here I entered my username (chrissie) but I used the wrong password (123 instead of 123chris). I then got the error as written in the code
<img width="596" alt="failcode" src="https://github.com/Chrissiez/students/assets/142445376/4cebd870-eb3e-436b-987b-8291479c8da2">

<img width="914" alt="failure" src="https://github.com/Chrissiez/students/assets/142445376/14b90cc3-a819-4350-8cec-5b9ed2081971">


