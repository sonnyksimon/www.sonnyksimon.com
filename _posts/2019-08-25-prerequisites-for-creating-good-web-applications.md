---
layout: post
charset: utf-8
description: Sonny Kothapally is a hacker. He is currently enrolled in a distance learning programme studying computers.
url: http://www.sonnyksimon.com/
locale: en_US
type: website
site_name: sonnyksimon
permalink: /weblog/:title
category: tech
---
I'm assuming that you're learning a new technology, say Vue.js or Rust (gasp!) and you kind of understand how the 
Internet works (it works by communicating data over a network connection, in what is called a port). 

**Basics**

 * *Hello World*

   The first thing you should learn is printing the text "Hello, world!" onto the screen. By this I mean that 
when someone visits your page running on your host machine (at localhost) on some port (8080?), i.e. at 
http://localhost:8080, they see "Hello World!". 

 * *Serving Static Files*

   The next thing you should figure out is how you serve `static files` -- files that you would
normally interact with on your filesystem. Typically this means just dropping a file (maybe style.css) into the project.
For instance, if I visit http://localhost:8080/style.css, it would be nice if I can just grab all your css styles.

 * *URL Handling*
 
   In URL handling, you need to figure out first how to map different routes to their responses (like we did with
 Hello, World!). Once you can get the text on  http://localhost/some-other-route/, you should learn how to define these
 routes using regular expressions (seriously, just use pattern matching from the outset). Once you really understand
 manipulating regex with your routes, then you should then figure out capturing parameters, which is pretty trivial once
 you've played around with regex matching.
 
 * *Redirection and Status Codes*
   
   You should then move on to figuring out how to redirect users to different URLs. E.g. If I visit 
http://localhost:8080/google/, that should redirect me to Google's search page. You typically redirect users by sending
the status code of 303 and now's a good time to figure out all the various status codes you can send (200, 404, 500, ..).

 * *Serving other types of data*
 
   Up until now, you should have been just sending raw text to the browser, which it decodes into either plaintext or
interprets it as HTML. Now is a good time to look at XML. Once you can serve XML, then dabble in JSON responses. These
are used alot in APIs nowadays. There's also a format called Notation3 which is pretty neat.
 
 * *Reading data from POST*
   
   Next figure out how to do what is called a POST request. This is what fires when someone clicks a button on your site.
You need to know how to read input fields, and manipulate the data that is returned from them. 

**Advanced**

 * *Contextual Variables*: Figure out how to gain access to the visitor's ip address, and their HTTP headers.
 
 * *Application Processors and Hooks*: Figure out how to add processors that do actions before and after a HTTP request.
 
 * *Background Processes*: Figure out how to create a separate background Thread which served a HTTP request and then
reports back a status to a function that `initiated` the Thread.

 * *Custom Not Found message*: Figure out how to return a 404 error message, for invalid routes.
 
 * *Streaming Large Files*: Figure out how to serve video content, and then how you make sure that the browser doesn't
need to buffer all the video content before serving it to you. You can also do this with say a really huge image, but
even though the data is sent in chunks, the browser typically waits for all the chunks unlike video content.

 * *Logging*: You should write all your logs to stdout (i.e. the console). What you then do is have another program, that
saves stdout to a log file (typically a file ending in ".log").

 * *SSL support*: Figure out how to redirect urls to https, and how to use a certificate file (and corresponding private 
key).

 * *Internationalization (i18n)*: Figure out i18n.
 
**Sessions and User State**

 * Creating sessions
 * Refreshing sessions
 * Handling Cookies
 * User authentication with builtin hashing libraries
 * User authentication with basic auth
 * User authentication with a database
 * Unpacking data from sessions

**Utilities**

 * Sending mail
 * Sending mail from gmail
 * SOAP webservices

**Templating**

 * Layout composition
 * Multiple templates
 * Using functions in templates
 * Concatenating two rendered templates

**Testing**

 * Application testing
 * RESTful testing using HTTP requests

**User Input**

 * File Upload
 * Storing uploaded files
 * Limits the size or filetype of uploads
 * Accessing user input
 * Rendering forms
 * Rendering individual form fields
 * Protect forms from CSRF attacks

**Databases**

 * Multiple databases
 * Select
 * Update
 * Delete
 * Insert
 * Advanced Queries
 * Database Transactions
 * Using ORMs

**Deployment**

 * Deployment on lighttpd
 * Deployment on Apache
 * Deployment on nginx
 * Deployment on a cloud service, like AWS or Heroku

[just a draft for now, to be completed later]
