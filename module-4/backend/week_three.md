## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?

Node is a JavaScript runtime that utilizes Chrome's V8 engine outside of the browser environment.

2. What is Express? Why is Express similar to in the Ruby world?

Express is a web application framework that sits on top of Node. It's similar to a framework like Sinatra in the Ruby world in that it gives us a lightweight and highly customizable framework with few limitations and opinions. 

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

```
app.get(<end point uri>, function(request, response){
   <function contents>
  })
```     
     
4. What do we use Knex for?

Knex is the object relational mapping tool we use in express. It allows us to interact with our Database.

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?

With regard to the express server we could divide our code into sections that model this more closely. Our server.js file could contain all of our endpoint urls that have specified callback functions. Those callback functions could live in a separate folder in files divided by resource. Here we would parse each request and generate a response by calling the model file for that resource. These model files with live in their own directory and would be responsible for querying the database and manipulating the data for their specified resource. This data would be handed back to the controller function, which would serve the response. 

6. How do you execute raw SQL in node?

```knex.raw('SELECT * FROM <table name>')```

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?

As always, there are trade offs. Some advantages to having your front and back end code live in separate applications relate to the separation of concerns. It allows both applications to be developed in isolation without neccessarily effecting one another. It makes it possible to write the back and front end in different languages or frameworks depending on the needs of the applciation. With a rest framework connecting them it also enables you to build multiple front ends that interact with the same backend or vice-versa. Some disadvantes porentially include having to validate users across two applications, chasing bugs through a larger and more separated code base and not being able to take full advantage of backend framework templating. 


#### Review  

8. Describe DNS.

Domain name servers hold a lookup of every human readble url and their corresponding ip address. When we type an address into a browser that url is parsed and the DNS is queried to find out what address to make the http request to. They are the internet equivelent of a phone book.

9. What does writing clean code mean to you?

The term clean code can obviously be very subjective. To me, in a general sense, it means clear and sensible variable and method naming, following the best practices of the language in terms of organization(putting shared methods in a module for example), not favoring the terse methods over readability and generally conforming to S.O.L.I.D. principles particularly keeping code DRY and modular.

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?

Room model which could hold the the room number, number of beds, total occupancy and room rate 

Reservation model which would could hold a creation date, an arrival date, checkout date, status, guest id and room id. It could also calculate stay length 

Guest model which would hold contact/billing information for a guest

Bill model which would hold guest id, payment status, line items and calculate total due at checkout

Line Item which could hold amenities or room rates and are held by the bill model

Amenity model which would be a type of amenity provided by the hotel as well as a cost for that item


