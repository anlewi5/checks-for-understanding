## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
  * GET: 'get' the stuff on the page
  * PUT: update data
  * POST: add new data
  * DELETE: remove data
  * HEAD: just get head information from the response
2. What is Sinatra?
  * Sinatra is a Ruby framework
4. What is MVC?
  * MVC stands for Model View Controller which is a way of seperating responsibilities
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  * To make things easier to understand/remember and to reduce error
6. What types of variables are accessible in our view templates without explicitly passing them?
  * COME BACK
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    erb :index
  end
  ```
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  * After internet research...
  
  ```ruby
  get '/horses' do
    @count = 1
    render locals: { name: "Mr. Ed" }
    erb :index
  end
  ```
9. What's the purpose of ERB?
  * ERB stands for Embedded Ruby and as the name suggests, it allows ruby code to be embedded in HTML code.
10. Why do I need a development AND test database?
  * You need both a development and a test database so that when the tests are run, dummy data used in the test is not added to the dev db.
11. What is CRUD and why is it important?
  * CRUD stands for Create Read Update and Delete and it outlines basic functionality when working with data.
12. What does HTTP stand for? 
  * HTTP stands for HyperText Transfer Protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  * ```<% evaluates as Ruby code but doesn't not render on the page %>```
  * ```<%= evaluates and renders %>```
14. What's an ORM?
  * ORM stands for Object Relational Mapper and ORMs allow easy use of different data types
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  * ActiveRecord. Probably. Since that's what we're learning.
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  1. Get '/index'
  2. Get '/show/new'
  3. Post '/show'
  4. Get '/show/edit'
  5. Put '/show/:id/edit'
  6. Delete '/index'
  7. Get '/show/:id'
17. What's a migration? 
  * A migration is when you move data into your database
18. When you create a migration, does it automatically modify your database?
  * No, not until you run the migration
19. How does a model relate to a database?
  * A model creates objects from database items and defines functionality for those objects
20. What is the difference between `#new` and `#create`?
  * New and create both add new database items, but only create saves the item in the database.
