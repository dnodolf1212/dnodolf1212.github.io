---
layout: post
title:      "Everybody's got choices (React & Redux or local state?)."
date:       2021-02-10 22:37:24 +0000
permalink:  everybodys_got_choices_react_and_redux_or_local_state
---


Logistically speaking, my Lookin' Sharp application wouldn't necessarily need to implement Redux to manage state. The beauty of react is that most components can keep track of state on a local level, utilizing Container Components to define and change state. A huge benefit to this local state is the reusable nature of a componentany where it's position isn't dictated by the parent or container component. An example is a clock component that updates its own state to keep track of the ticking seconds as they go by. Its counter is its state, and the function running the passing of time simply updates those seconds INSIDE the component itself. We could put a clock on every page of our application if we wanted. Yet, time is a construct of man, so we shouldn't.
In the case of the final project, the use of a redux store did give us insight into how these components would be offered a more centralized state, so our use of props didn't have to flow through several components. In terms of mutable state, being able to change state with the use of this store, the process is a bit more involved. The stand alone container components need to connect to the store, and importing and implementing the necessary Connect, Compose, ApplyMiddleware, Thunk, etc. which gives us a means to map State and Dispatch to props. Essentially, we've given this component access to the entire Application State and ability to pass the dispatch function to a reducer -- a sort of central hub where functions turn into actions that change state. With this configuration we can leap-frog over all these other components, which Im told is the case in large scale applications, and change state without including the necessary functions and variables as props down through every subsequent component. 
