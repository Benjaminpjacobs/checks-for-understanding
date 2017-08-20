## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?

I really dug the lodash and underscore libraries. Also really diving in to ES6 syntax and the power of arrow functions has been very useful.

2. What are some tools to help debug JavaScript code?

pryjs, debugger, chrome dev tools

3. What are some tools you need in order to unit test your JavaScript?

Mocha, Chai, Selenium if you are integration testing

4. What is the syntax for invoking a function?

myFunction()

5. What's the difference between `==` and `===` in JavaScript?

With the == operator no type conversion is done. That means 1 == '1' //=> true but 1 === '1' //=> false. Generally it is better practice to use === in JS.

6. What's the difference between asynchronous and synchronous JavaScript? 

Synchronous JS works more like ruby in that one action follows the next after completion. Asynchronous JS works differently in the sense that the next action will not wait until the previous one is completed.

7. What's a callback function and what are some reasons when we use/need callback functions?

A callback function is a function that is passed to another function and called backed to at some future point. We use them often in jQuery or with event listeners in javascript. For example if we have a node that we add a click event to we will pass it a callback function to tell the eventlistener what to do after the event is fired. $(node).on('click', callBackFunction).

8. What's the biggest difference between a promise and a callback?

There are many, but my best guess would be that a callback function can return data but a promise can only return a promise. Thus once you are in a promise chain, you have to call actions within the chain because you cannot explicity return data from them. Additionally promises allow you to take different trajectories based on the success or failure of the action which invoked the promise i.e. an ajax call will have success functions and failure functions based on the status of the response.

9. How do we setup a route when creating an API with Node and Express?

I don't specifically know yet. But a quick search throught the lesson one week from today tells me: it's something like this:

```
app.get('/', function(request, response) {
  response.send('It\'s a secret to everyone.')
})
```

10. What's `npm` and what do we use it for?

Node Package Manager. It is a bit like bundler in ruby. It installs our dependencies, runs our server, handles webpack, etc.

#### Review  
11. What's the MVC design pattern? Describe each part of MVC?
Model, View, Controller.

The view is the front end template usually composed in some form of html with embedded capabilities it is responsible for how a page will be rendered, what it will look like and how content is organized.

The controller literally controlls the flow of traffic. Based on how the routes or uris are setup different controller actions will be called which query information from the database, models and other class objects and package and send that information to the view

The model is the building block of the database backed MVC application. It literally models an object that exists in the databse determining what attributes it will have and ways to manipulate that data.

12. What is AJAX? What are some benefits of using AJAX?

Asynchronous JavaScript and XML. The benefits of ajax are that it is asynchronous meaning it will not stop the application in order to retreive data, thus the user can continue performing actions on a page while data is being gathered in the background. Additionally it has a level of fault tolerance by giving developers a means to handle returned errors without crashing the application.

13. What's a background worker? When would we want to use a background worker?

A background worker, in Rails specifically, is a class of object that can work asynchronously to the main actions of the application. They can be fired off immediately, intermittenly, or at some point in the future and handle tasks that do not need to be synchronously performed. A perfect example is background mailers. One could use a background worker to send out confirmation or reminder emails to users because these actions take time to perform and shouldn't require a user to wait for them to be completed.
