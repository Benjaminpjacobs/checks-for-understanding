## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
Get, Put, Post, Patch, Delete
2. What is Sinatra?
Sinatra is a framework for making lightweight web applications.
4. What is MVC?
Model View Controller
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
Firstly, in order to closely model what we will be using in rails. Also in order to have the actions/paths be consistent with conventially http calls.
6. What types of variables are accessible in our view templates without explicitly passing them?
Instance variables.
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = Horses.counta.
    @name = 'Mr. Ed'
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  
9. What's the purpose of ERB?
ERB allows us to interpolate ruby into an html document allowing us to dynamically render content in the browser.

10. Why do I need a development AND test database?

Because the test database allows for tighter control over what elements will exist in it at any time allowing for stronger testing scenarios. Also, so we do not permanently alter any production dat

11. What's responsive design?
This referes to css design that responds to changing browser screen size effectively and dynamically(without reloading).

12. What is CRUD and why is it important?

Create, read, update, delete. It is the foundation of all actions one can perform on a database.

13. What does HTTP stand for? 

HyperText Transfer Protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

`<%= This will interpolate the return value %>` , `<% This will run the code, but not interpolate the return value %>`

15. What's an ORM?

Object Relational Mapper. In our case this is Active Record. It allows us to create objects out of data or collections of data in order to interact with them like ruby objects(i.e. call methods on them).

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?

Active Recrod.

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

`get '/index'` - This shows a list of all the restaurants
`get '/index/id'` - This shows a specific restaurants
`get '/index/new'` - This is a form to create a new restaurant
`put '/index/id'` - This submits and creates the new restaurant
`get '/index/edit'` - This is a form to edit a new restaurant
`post '/index/id'` - This submits the changes for the restaurant
`delete '/index/id'` - This deletes a restaurant




18. What's a migration? 

Migration is what is performed when moving a database between machines. It effectively creates the data tables based on a series of migration files and allows for exact database conditions to be transferred between environments.
19. When you create a migration, does it automatically modify your database?

No. You have to run the migration for it to make changes.

20. How does a model relate to a database?

Every table in a database has to have an associated model. The model effectively creates the settings for each table in terms of validations and associations and methods that can be performed on objects originating from those table rows.

21. What's the difference between agile workflow and waterfall method?

Waterfall performs the four stages of development in successive order to completetion. Agile performs all four stages in iterative stages of completion.

22. What is the difference between `#new` and `#create`?

New creates an object but does not automatically save it to the database. Create makes an object and saves it to the databse.
