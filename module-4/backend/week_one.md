## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the 
majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?

The most useful thing I leaned over intermission week was how to utlizie the newer ES6 arrow function syntax.

2. What are some tools to help debug JavaScript code?

pryjs, debugger, chrome dev tools

3. What are some tools you need in order to unit test your JavaScript?

Mocha, Chai and Selenium if you are integration testing

4. What is the syntax for invoking a function?

myFunction()

5. What is CORS?

Cross Origin Resource Sharing it is a standard that allows HTTP requests between different origin sites.

6. How do we enable CORS?

We must configure the server to respond to requests from other domains with an Access Control Allow Origin in is preflight response.

7. What's `this` in JavaScript?

This is a self referential objection that refers back to the context in which it is called. 'This' changes value fequently depending on this context.
Globally, for example, 'this' refers to the window. Within a constructor function 'this' refers to the new object that will be instantiated by the
contructor. In an Arrow function 'this' will refer to the conext in which the function was invoked. Those are just a few examples of the possible
meanings of 'this'.

8. What is Webpack and why is it useful?

Webpack is a tool that helps to manage our dependencies with client-side JavaScript. It is useful because it allows use to require single bundled
JS that create a pipeline for our aset hierarchy as well as delivering minified JS and CSS files to the client browser.

9. When/why do you want to use event delegation?

Event delegation is used when there is a need to add an event listerner to an element that may not initially be loaded on the page. Event delegation
allows us to bind these event listerners dynamically while protecting us from memory leaks caused by adding event listenrs to elements that are
not or are no longer on the page.

10. What is a callback function?

A callback function is a higher order function in that it is passed to another function. It is referred to as a callback becuase the initiating
function will call back on it at some future point. We use them often in jQuery or with event listeners in javascript. For example if we have a 
node that we add a click event to we will pass it a callback function to tell the eventlistener what to do after the event is fired. 
```$(node).on('click', callBackFunction)```

11. What's `npm` and what do we use it for?

Node Package Manager. It is a bit like bundler in ruby. It installs our dependencies, runs our server, handles webpack, etc.

#### Review  

12. What's the MVC design pattern? Describe each part of MVC?
Model, View, Controller.

The view is the front end template usually composed in some form of html with embedded capabilities it is responsible for how a page will be 
rendered, what it will look like and how content is organized.

The controller literally controlls the flow of traffic. Based on how the routes or uris are setup different controller actions will be called 
which query information from the database, models and other class objects and package and send that information to the view

The model is the building block of the database backed MVC application. It literally models an object that exists in the databse determining 
what attributes it will have and ways to manipulate that data.

13. What are a few ways to optimize a Rails application?

One of the primary ways to optimize a Rails application is with fragment and low level caching. Using the rails cache to store partial responses 
of view-related data or typical DB query results will help optimize page load time. Lazy-loading of large database queries which can be used in conjunction with pagination
will also help with page-load time. Additionally, unitliizng optimal active record query syntax will help keep the flow of data as efficient as possible.

14. What's a background worker? When would we want to use a background worker?

A background worker, in Rails specifically, is a class of object that can work asynchronously to the main actions of the application. 
They can be fired off immediately, intermittenly, or at some point in the future and handle tasks that do not need to be synchronously 
performed. A perfect example is background mailers. One could use a background worker to send out confirmation or reminder emails to users 
because these actions take time to perform and shouldn't require a user to wait for them to be completed.

