# Interview-Practice-Full-Stack
Interview Practice questions from Udacity Full Stack Nanodegree

1.<i><b> What is the most influential book or blog post you’ve read regarding web development?</b></i><br>
I have not personally read a book or blog post regarding web development that was influential to me. My influential moments that got me interested in web development was through my introduction at school. In high school, I took a web design course. When taking this course, I became inspired by things you can create on a website and how creative you can be. This would be the only time I would be work on web designing. Later on when I went to college, I was introduced to programming such as Java, C++, and C#. Once being learning programming, it ignited that same passion I had when I was making websites back in high school. Eventually, I would run into a professor that wanted to work on a project with a couple students outside of class. The project he wanted to make was programming quiz mobile app using HTML, CSS, Javascript, Ionic Framework, and Apache Cordova. While working on this project with him, this further opened my eyes more to the things you can do with web development. Previously, I was under the assumption that you can only make websites. But now, I see that through web development you can create a web application that can easily transition from the web to mobile environment using the same code that works on any environment. Also while working on this project, I got to see and dabble in the two sides of web development which are Front-End and Back-End Web development. I got to understand how the Back-End stores the data that will be later used to be served to the Front-End of an application. After learning Front-End and Back-End that is when I discovered that I wanted to become a Full Stack developer and participate in both sides in the web application creation process.


2. <i><b>Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?</b></i><br>
A web application I built was Multi-User Blog as a project for the Udacity Full Stack Nanodegree. The functionality of this application is a blog website that allows users to create posts as well as edit and delete them, and also like and comment on other user's posts while logged into the blog.

While building this project, I learned about the concepts for Back-End Development (such as CRUD), Jinja2 framework, Google App Engine, and authorization and authentication of users with access to creating, reading, deleting or updating data stored in a database. 

The challenges that I faced was learning and utilizing new frameworks, and  understanding how the back-end of an application works. With my experience in developing front end applications previously, the debugging errors were more apparent in the code. While working on this project, I received multiple debugging errors that pointed to external libraries that left me clueless in where to start debugging. So I learned how to analyze the error messages in order to break down my code and perform unit tests using trial and error to precisely pinpoint where an error occurs. I would reference the documentation for Google App Engine as well as Google or Stack Overflow to see if anyone else ran into a similar problem. This project for me has truly was a stepping stone into bettering my skill as a programmer as it gave me rigorous test of learning a new language and learning how to debug errors through testing.


3. <i><b>Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list (< ul > ... < /ul >) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?</b></i>

```
## Interview Practice
## Question 3
## Unordered HTML List using Python

list = ["apple", "orange", "banana", "grapes"];

def mylist (list):
    htmllist = "My list of fruits: "
    htmllist += "<ul>"
    for i in list:
        htmllist += "<li>" + i + "</li>"

    htmllist += "</ul>"

    return htmllist

mylist(list)
```


This code takes in a Python list within a function. The function contains a for loop that will iterate through the list an display each element in an unordered list.

Things to consider if a user input the data for list:

- If the user enters any data that is not a string. To resolve this we would need to sanitize to check the user's input to make sure they input the correct data type. This can be done through some conditional statements also.

- Any HTML/Script injection. To prevent this, we will have to escape any data inputted by the user.
<br>

4. <i><b>List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks? </b></i><br>
Two attacks that web applications are vulnerable to are XSRF cross domain and SQL injection attacks. 
•	An XSRF attack is a cross site request forgery. The attack uses the information stored in a cookie in the user’s browser to make unauthorized HTTP requests. This can be prevented through generating an access token that must match the server’s token in order to complete a request. An example of this would be the CAPTCHA field used on some websites when trying to access a certain page of a website.
•	SQL Injection attack is an attack by the user injecting SQL code into input fields in order to manipulate data in the database. This can be prevented through multiple ways. One the ways would be using pre-built functions that perform SQL Queries instead of creating whole SQL queries based on the user’s input. Another way is performing data sanitization on the user’s input and escaping any values entered. An additional prevention technique can be limiting the database privilege a user has to perform actions in the database.


5. <i><b>Expand on the starter code and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.</b></i>
```
from flask import Flask
from flask import Flask, render_template, request, redirect, jsonify, url_for, flash
import httplib2
import json
import random
from flask import make_response
import requests

app = Flask(__name__)

@app.route('/')
def hello_world():
 return 'Hello World!'

@app.route('/diceroll')
def diceRollJSON():
    # MenuItems = session.query(Movie).filter_by(
    #     category=category).all()
    dice1 = random.randint(1, 6)
    dice2 = random.randint(1, 6)
    diceroll = dice1 + dice2
    return jsonify(
        dice1=dice1,
        dice2=dice2,
        diceroll=diceroll
    )

if __name__ == '__main__':
 app.debug = True
 app.run()
```

This code uses Flask and random python libraries. Flask is used to perform the URL routing within the application. To get the result from a simulation of two dice rolls, there are two variables that represent each dice that sore a random integer value between 1 and 6 using the randint() function from the random library. Then the values stored in each dice variable are added together, and the sum is return as a JSON object.


6. <i><b>If you were to start your full-stack developer position today, what would be your goals a year from now?</b></i><br> 
A year from now, I would like to have more experience/knowledge as well as understand how my Full Stack knowledge can be implemented into a production environment. I want to be able to learn from those that are well skilled in the company as well as share my new-found knowledge to other up incoming developers within the company. I would like to be able to contribute to a team and become integral part of the team. Another goal would be to have increased familiarity with Django framework and back-end languages such as PostgreSQL, and learn any other technologies that potentially make running and maintaining the web and mobile applications more easier or efficiently.
