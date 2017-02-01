#flask-club
A web server using Flask to maintain a list of user profiles. Join the Flask Club and get your own profile page on the server!

###Objective

Students will use a framework called Flask to build a web server that can handle both GET and POST requests. Users of this server can create a profile on the server which is accessible through the browser. Students will use Flask's HTML template capabilities to create and present dynamically generated pages based on the parameters of the request.

###Prerequisites

In order to complete this exercise, students should have the following:
- Understanding of the available HTTP request methods
- Understanding of how an HTTP request is structured
- Familiarity with how to make a POST request in Python
- Familiarity with how web servers receive and respond to requests

###Requirements

- flask and its dependencies, available via pip
- If you are on Python version 2 that is 2.6 or newer, or on 3.3, you are ready to use Flask. 
  - Otherwise, you may need to install `python-virtualenv` and run it on one of the supported Python versions. Flask does not support Python 3.2.
- [Installation guide](http://flask.pocoo.org/docs/0.12/installation/#installation)

###Desired outcomes

Students will complete this exercise with a better knowledge of how web servers work, how to have a server handle different types of requests, how to dynamically serve content based on the parameters of the request, and how to use a framework to make common development tasks simpler.

###Your challenge

1. Create a new directory for your Flask server. Inside, make a Flask server or start with the example code provided. By default Flask runs on port 5000.
2. Create a route for `/user/` that accepts a POST request. Flask has tools for accessing the body of a request that may help you. The POST request will contain some data, such as a username, a favorite food, and a short message of the user's choice. Keep track of this data somewhere.
3. Create a directory `templates` inside your server's directory and make a file `user.html` inside the `templates` directory.
4. Fill out `user.html` using [the Jinja template docs.](http://jinja.pocoo.org/docs/templates). Include fields for username, favorite food, and message.
5. Create a route for `/user/<username>` that will render your HTML template using the data on file for that user. Pass the template renderer the necessary parameters from your data.

The end result will be, if NyanCat sends a post request to `/users/` with a username, food and message, going to `http://[your ip]:5000/users/NyanCat` will display an HTML page with NyanCat's information.

#####Extras
6. Make sure your server can handle the case when trying to access a user page when that user hasn't created a profile yet.
7. Implement a password so that only users who know the password can create pages. Reject any requests without the password.

###Resources
[](http://flask.pocoo.org/docs/0.12/quickstart/)
