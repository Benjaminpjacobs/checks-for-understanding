## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6?

The use of fat arrow function whcih bind 'this' wherever the function is initiated is one of new features of ES6
  
2. What's the difference between asynchronous and synchronous JavaScript? 

Synchronous actions happen in succession and only once the previous action has been completed. Asynchronous actions are     initiated and then the next action is initiated immediately. These action return in the order in which they are completed, i.e. however long any action takes will determine the order in which it returns.

3. What are the four pillars of Object Oriented programming?
Abstraction, Polymorphism, Inheritence, Encapsulation

4. What are some tools available in JavaScript to help you write object oriented code?
Things like constructor functions and es6 classes encourage the writing of more object oriented code. Additionally closures can help us gain the functionality of private methods in our JavaScript code.

5. What are some key concepts to be aware of when refactoring your JavaScript?
Understanding lexical scope, when and what a function will return and whether the functions are asynch or synch are all important concepts to keep in mind when refactoring JavaScript code

6. What's a callback function and what are some reasons when we use/need callback functions?
A callback function is one that is passed into another function as an argument that can be called later inside the function. We need to use callback functions in event listerners, for example, as a way of performing a function after an event is fired. Callbacks are useful in all sorts of asynch functions in order to tell the code what to do when data is returned. 

7. What's the scope of variables in Javascript?
Javascript variables can be either global or local. Varibale created outside a function are in the global scope and available anywhere. Functions create local scopes where variables created within are only available within the function and functions nested inside them. Lexical scope is this heirarchy of variable lookup from the most local to the global.

8. What's the difference between `==` and `===` in JavaScript?

The `==` will match across data types where as `===` will look for an exact type match. For example:
```
1 == '1'  //=> True
1 === '1' //=> False
1 === 1   //=> True
```
9. Why do front end frameworks exist?
As more of the code developers write is moving to the client side to improve speed, performance and user experience the need has arisen for front end frameworks that offer developers tools to larger more complex programs in an organized way. Front end framewoks make complex tasks easier and allow for the development of applications that conform to SOLID principles.

#### Review  

10. Why do people say "HTTP is stateless"?
HTTP is referred to as stateless because it does not persist any information between calls. Through a request or response contains data it does not hold any of this data in variables that will last beyond a single cycle. Additionally one cycle of request/response does not know about the previous one or the next one. 

11. Describe a RESTful API.

A RESTful API is one that conforms to the standard HTTP verb conventions for different types of requests. It will offer endpoints that utilize GET for retreivin records, PUT/PATCH for updating records, POST for creating records and DELETE for destroying records. In this way the request actions are universaly understood allowing for the smoothest interface for consumers of the API.

12. What are some main characteristics of a team following an agile workflow?
Teams that follow agile practices will tend to break up their projects into sprints, or shorter bursts of productivity with a clearly definied and ideally acheivable goal. These will be managed by a team lead or product owner or combination of the two and often involve daily standups in which each member of the team quickly recounts their tasks completed the previous day, tasks to complete today and any block items that are preventing them from completing their piece. In this way they are able to remain flexible and response to changes that may occur or to course correct when neccessary. 

13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
Using OAuth to authenticate a user allows the developer to effectively outsource the authentication process. It can save a lot of code and a lot of time by utilizing the authentication features of an exterior service and can make the interface more convenient for the user by allowing them to have fewer overall login credentials. It also has the advantage of giving the developer access to information related to that user from the external service(i.e. OAuth through github would allow for access to repo data etc). This however can also be a disadvantage. Depending on the service through which OAuth is done one may not gain all the information that they require and generally has less contorl of what data you get and how it can be manipulated. Additionally there is always the chance that the service being used for OAuth may cease to exists leaving the users no recourse for accessing their data.
