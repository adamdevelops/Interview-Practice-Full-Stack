# Interview-Practice-Full-Stack
Interview Practice questions from Udacity Full Stack Nanodegree

1. What is the most influential book or blog post you’ve read regarding web development?
I have not personally read a book or blog post regarding web development that was influential to me. My influential moments that got me interested in web development was through my introduction at school. In high school, I took a web design course. When taking this course, I became inspired by things you can create on a website and how creative you can be. This would be the only time I would be work on web designing. Later on when I went to college, I was introduced to programming such as Java, C++, and C#. Once being learning programming, it ignited that same passion I had when I was making websites back in high school. Eventually, I would run into a professor that wanted to work on a project with a couple students outside of class. The project he wanted to make was programming quiz mobile app using HTML, CSS, Javascript, Ionic Framework, and Apache Cordova. While working on this project with him, this further opened my eyes more to the things you can do with web development. Previously, I was under the assumption that you can only make websites. But now, I see that through web development you can create a web application that can easily transition from the web to mobile environment using the same code that works on any environment. Also while working on this project, I got to see and dabble in the two sides of web development which are Front-End and Back-End Web development. I got to understand how the Back-End stores the data that will be later used to be served to the Front-End of an application. After learning Front-End and Back-End that is when I discovered that I wanted to become a Full Stack developer and participate in both sides in the web application creation process.


2. Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?
A web application that I have built that really sticks with me is the Multi-User blog that I designed using Google App Engine. This is an application that I’ve done in part of the Udacity Full Stack Nanodegree to learn about the concepts of Back-End Development, and authorization and authentication of users with access to creating, reading, deleting or updating data stored in a database. The challenges that I faced was learning how the backend of an application works and understanding the way Google App Engine worked for the first time. I can honestly say that this project took me the longest time to complete. I had to spend most of my time reading the documentation of Google App Engine to comprehend how data flows in Google App Engine using the built-in functions. When working on the Back-End of this application, the data flow isn’t as transparent compared to when I was creating applications for the Front-End. Another element that affected the amount of time I spent on this project was debugging errors. In referencing how the data flow is more transparent in the Back-End so were the errors. I received multiple errors over the course of the project that pointed to an external library in Google App Engine instead of an exact line within my code. To solve these errors, I had to analyze how data was processed in a particular part of the application, and use trial and error to see at which point in the code breaks and errors out. After seeing where my error occurs, I would reference Google or Stack Overflow to see if anyone else ran into a similar problem. This project for me has truly was a stepping stone into bettering my skill as a programmer as it gave me rigorous test of learning a new language and learning how to debug errors through testing.


3. Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list (<ul>...</ul>) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?

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

4. List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks? 
Two attacks that web applications are vulnerable to are XSRF cross domain and SQL injection attacks. 
•	An XSRF attack is a cross site request forgery. The attack uses the information stored in a cookie in the user’s browser to make unauthorized HTTP requests. This can be prevented through generating an access token that must match the server’s token in order to complete a request. An example of this would be the CAPTCHA field used on some websites when trying to access a certain page of a website.
•	SQL Injection attack is an attack by the user injecting SQL code into input fields in order to manipulate data in the database. This can be prevented through multiple ways. One the ways would be using pre-built functions that perform SQL Queries instead of creating whole SQL queries based on the user’s input. Another way is performing data sanitization on the user’s input and escaping any values entered. An additional prevention technique can be limiting the database privilege a user has to perform actions in the database.


5. Expand on the starter code and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.
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


6. If you were to start your full-stack developer position today, what would be your goals a year from now? 
If I was to start as a Full Stack developer today, my goals in a year from now to have more experience/knowledge as well as understand how my Full Stack knowledge can be implemented into a production environment. I want to be able to learn from those that are well skilled in the industry. Over this year, I plan on cementing my knowledge of Back-End development through working with SQL, and getting a better understanding what SQL version is better for an application that you are trying to build. I would like to learn more MV (Model View) frameworks that dynamic update without a page reload more so in particular React JS. React JS is widely used and I feel it would be valuable for me to know, and it seems to have a great supporting community thus showing it will have a continued space in web development. Another goal of mine is to create more projects on my own and with other developers.
