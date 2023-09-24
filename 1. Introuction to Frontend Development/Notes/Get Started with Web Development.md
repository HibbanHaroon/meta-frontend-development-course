## Important Topics Covered
1. Response-Request Cycle
2. Hyper Text Transfer Protocols
3. Frameworks and Libraries
4. Refactoring

# Get Started with Web Development

### Introduction
Firstly, I was introduced to what we will be learning throughout the Meta Frontend Developer course such as HTML, CSS, JavaScript, Version Control, React etc. Then, I learnt what we will be learning in this Introduction to Frontend Development course. 

Things I will learn will be:
1. What are the roles in web development such as Frontend Developer, Backend Developer, Full-Stack Developer.
2. Basics of HTML, CSS
3. Bootstrap
4. How the web works
5. What is React

### How the web works?
Computers are connected together with switches and switches are connected to other switches forming an interconnected network called Internet. How do we communicate? Well, See it as like this, If you search a question on your browser. It returns the response in no time. You are the client talking to the Internet and you got your response back from a server.

##### Server
Server provides service to the clients. Servers are stored on Data Centers. You get your information from the nearest server. Web server - a type of server handles your web requests. They bring you the content of the website as you load them. It's responsibility is to also handle multiple user requests as one and to manage security, website storage and administration.

##### Websites
Websites are made up of webpages. Webpages are built using HTML, CSS, JavaScript.

HTML - Structure of the website
CSS - Styling of the website
JavaScript - Interaction of the website
###### HTML
HyperText Markup Language which uses markup tags like h1 and p etc.
###### CSS
Cascading Style Sheets used for styling the elements of the webpage.
###### JavaScript
Programming Language used for interactions with the elements of the webpage.
###### Page Rendering
Code from the web server is processed in sequential order and displayed on the browser for the user. Browser engine is used for page rendering.
###### Response-Request Cycle
You open a browser. Search the URL like www.google.com. The webserver sends you the code of the webpage which is rendered and then displayed to you. This is the first request-response cycle. You then type in the search bar of google like "What is a response-request cycle". This request is sent to webserver where it is processed and sent to the database to fetch the relevant data. Webserver gets the result from the database and then sends you the webpage code with the result in it. This webpage is then rendered for you to see your results. This is another response-request cycle and it can go on and on. 

### Core Internet Technologies
I learnt how IP Addresses work and how TCP - a protocol used for images and text so that the packets being transmitted arrive in order, without lost and damage to the destination and UDP - a protocol used for live streams or calls where some data lost is acceptable. 

##### Hyper Text Transfer Protocols (HTTP)
A Communication Protocol used when communication between the client(web browser) and the server(web server).
###### HTTP Request
GET / HTTP/1.1
Host : developer.mozilla.org
Accept-Language: en

Different methods are GET, POST, PUT, DELETE
###### HTTP Request
HTTP/1.1 200 OK
...
###### HTTP Status Codes
Informational 100-199
Successful 200-299
Redirection 300-399
Client Error Messages 400-499
Server Error Messages 500-599
###### HTTPS
A secure version of the HTTP. It uses encryption so that nobody else can understand the message being transmitted. 

##### Difference between Websites and Web Applications
Web applications are more dynamic, interactive and offer personalize content to the users. On the other hand, Websites are just used for informative purpose like a landing page for a company. 


##### Difference between Frameworks and Libraries
###### Libraries
Libraries provide re-usable code so that you don't have to re-create the code from scratch. It saves time and effort. For example, using Toastify library is one example.

###### Frameworks
Frameworks handles functionalities that is common to all web applications like handling HTTP requests. It provides structures for developers to built with. It has many best practices already in place. The developer can add their own functionalities to make their website work like adding a text inputs and buttons to a form.

Frameworks uses libraries. Applications directly can use other libraries as well. 

##### REST API
RESTful API is an architectural style an API can conform to.

##### Refactoring
Changing the structure of the code without changing the functionality. For example, changing the name of function across different files.