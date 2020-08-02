---
layout: post
title:      "Figuring Out HTTP"
date:       2020-08-02 23:04:23 +0000
permalink:  figuring_out_http
---


The Sinatra Porfolio Project presented me with the opportunity to create something more utilitarian than the CLI Gem project. I could make something useful, that kept things organized and followed the same RESTful conventions used in applciations I use everyday. The applications use HTTP (Hypertext Transfer Protocol) requests, I describe as these individual, isolated calls and responses that collaborate with a Model, View, and Controller model. The MVC model lets us Create, Read, Update and Delete information stored within a database. 

How does it all fit together though?!

Upon visiting the app online, it sends a get request, an HTTP request to a path that produces a page we create in the Views part of our MVC model. In this case get '/' brought us to a welcome page with links to Log In or Sign Up. These links also send get request to /login or /signup but really are paths to pages that have Log In or Sign Up forms on them. These forms are fields, spaces that a user can enter their credentials and either create an account or gain access to an existing account. When we hit LogIn or SignUp from these forms pages, we are actually sending an HTTP Post request, to a path that will show us our recipes. Get and Post are the two mainstains of the HTTP requests. You are either GETting resources or POSTing to resources to gain access-to or view your information. 

