---
layout: post
title:      "A sum of its parts"
date:       2020-12-10 06:56:52 +0000
permalink:  a_sum_of_its_parts
---


The Rails/ Javascript project continues a paradigm of abstaction and modulization (sp?) that describes a system of many parts. These parts, models, controllers, api service classes, Javascript object classes, etc. all work together to connect a front end display to a backend database. The calls we make request data in the form of Ruby hashes. Objects composed of key value pairs, making up the attributes of one instance of a model. The way we get them to the viewer however, is quite a bit more complex. Enter fetch(), a function that calls our API (where we have all our data) and gives us a response in the form of JSON. Javascript Object Notation is the data returned from a fetch call, and we can utilize that to instatiate objects for our frontend. The classes in our "components" directory make up the creation department that takes these JSON objects and casts them as data we can see. Given behavior and attributes defined as functions and variables, the page we see as users can be populated with this data, as objects, and we can consume or manipulate them with the functions defined in their respective classes. 
