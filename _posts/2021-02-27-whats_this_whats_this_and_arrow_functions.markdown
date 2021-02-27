---
layout: post
title:      "Whats this! Whats THIS! (and arrow functions)."
date:       2021-02-27 05:56:24 +0000
permalink:  whats_this_whats_this_and_arrow_functions
---

The true nature of THIS depends on context. In the wild, without being bound to something, THIS will be Global, referencing the Window object, and in the Global scope, with a capital G. 
In a function we need to apply call, apply and bind to set the value of "this" into the scope of the function. Without explicity setting this value, the global scope is the default context.
Inside objects using "this" will refer to the object itself. Handy if you want to refer to the objects own values in the objects own methods. An all encompassing reference to itself. 
In React class components we will write methods that refer to class attributes like this.props and this.state. Binding the context of this in the component onto those methods is key but can be long winded or confusing. 
Enter ES6, with arrow functions that come pre-bound to "this" allowing us to use public class fields that bind "this" to methods. Their appearance is a sort of short handed function without the trappings of a return statement or parenthesese and this makes them somewhat more straightforward and readable. In my own experience, a great deal of value comes from arrow functions, especially when inside our React render function, the gateway to seeing our data on the DOM. Passing functions into React elements, we can preserve "this" using an anonymous arrow function and passing it by reference. Our arrow function will refer to it's own defined reference to "this" (wherever we defined said function) and carry it's context along from within our render function. However, this function will be re-created with each render of the component, which will break optimizations because of strict identity comparison. 
The rules aside, I like arrow functions for their ability to pass along parameters to callback functions. You want to delete something from that list you rendered? Pop an anonymous arrow function into that onClick event handler. The anonymous function allows us to pass in that delete-able item, and we dont have to directly invoke it! In this case, "this" references the function itself, defined outside of our rendering business. 

