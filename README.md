# full-stack-dry-run

Question 1 - What is the most influential book or blog post you’ve read regarding web development?

“How 3 Web Developers Built Careers from Scratch” is a Udacity blog series that profiles three of Udacity’s top web developers. Each post tells the story of a successful developer coming from a different, sometimes completely unrelated, background. My main takeaway from reading the blog is that web development is a fast-paced and constantly changing industry where continuous learning is paramount. As a self-starter who loves learning new things, this blog series was influential on me by helping me decide to start my first Udacity Nanodegree, the Introduction to Programming certificate. Now, in just a little over six months, I have completed three nanodegrees with Udacity, and have started looking for jobs.


Question 2 - Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?

A couple of months ago I built my first web application using the Flask framework, a content management system called “Catalog app”. Here is my code on GitHub: https://github.com/robertozanchi/catalog-app. I built this app as part of my Full Stack Web Developer Nanodegree studies at Udacity, in order to learn to use authentication and authorization functionalities. The most challenging aspect of this project for me was applying a broad range of skills to building a fully functional web app from scratch, combining design and queries into persistent data storage, use of a web application framework and the design of an HTML front end. This is something I’d never done before. I overcame this challenge using an “iterative development” approach” I learned from my Udacity courses. By applying a step by step, iterative approach I was able to create HTML template mock-ups, routing, templates and forms, database functionality and API endpoints, for the web app, and create a fully functional web application.


Question 3 - Write a function that takes a list of strings and returns a single string that is an HTML unordered list (<ul>...</ul>) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?

def create_list(strings):
	start = “<ul>
             ”
	list = “”             
      for item in strings:
		list = list + “<li>%s</li>
” % item
	end = </ul>

return start+list+end

The function create_list, written in Python, generates a simple unordered list of items passed into the function as the list strings. The list of items is created through a for loop that iterates through the list and creates a string with the HTML code for individual items in the list by means of string substitution. The function returns the list of individual items enclosed in <ul> and </ul> tags, as a string that is a simple combination of strings start, list and end. 

If users provide the input for the string, one would need to consider doing user input validation. Methods of validation of user input include:
-	Controlling user input with verification functions
-	Using string substitution combined with HTML escaping (e.g. Python’s built-in function)


Question 4 - List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks?

Two attacks that web applications re vulnerable to are injection attacks and the exploitation of insecure direct object references.
-	Injection attacks: can occur with non-validated user input, when a user deliberately provides as input code that performs a malicious command that affects the application’s backend. For example, non-validated JavaScript input can be injected to modify HTML forms.
-	Exploit of insecure direct object references: can occur when a user is able to modify values of a request, for example a URL in the browser, and access am object or a web page that she isn’t authorized for. Objects must be made inaccessible to unauthorized users.

Question 5 - Here is some starter code for a Flask Web Application. Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.

I have modified the code below to use the jsonify package and return JSON serialized object from a list. After importing jsonify from Flask, I created a new app route /dice/JSON. A get request now calls the function roll_two_dice, which generates random integer values between 1 and 6, and puts them into the rolled_dice list. The list is serialized as JSON in the return statement using jsonify. Code below.

from flask import Flask, jsonify

app = Flask(__name__)

import json
import random

@app.route('/')
def hello_world():
return 'Hello World!'

@app.route('/dice/JSON')
def roll_two_dice():
die_one = random.randrange(1, 7, 1)
die_two = random.randrange(1, 7, 1)
	rolled_dice = [die_one, die_two]
	return jsonify(i.serialize for i in rolled_dice)	

if __name__ == '__main__':
app.debug = True
app.run()


Question 6 - If you were to start your full-stack developer position today, what would be your goals a year from now?

Full-Stack Developer
Brooklyn, New York, United States
DESCRIPTION
Matter is pioneering small-batch manufacturing on the web and looking for a full-stack developer to help build out our end-to-end manufacturing platform. As lead developer, you'll work closely with our CTO and operations team to build both client and factory facing software. You'll be joining a small team in a pivotal role and have the opportunity to tackle challenges (spanning hardware, software and operations) that very view other technical roles encounter. This has the potential to evolve into a CTO or VP level position.
REQUIREMENTS
•	Must have 2-3 years experience building scalable web applications
•	Must be familiar with agile development and have experience using git
•	Must be comfortable with our software stack (MongoDB, Python, JS)
•	Must be willing to learn new skills and frameworks

One year from now, I aim to be able to create a product-grade scalable web application with mastery of the full stack of technologies involved. 

I aim to be able to be fully proficient git and the collaboration features of GitHub, have advanced skills in backend development in Python and further my knowledge of front-end technologies.
