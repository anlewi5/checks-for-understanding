## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

	```
	rails new app_name
	```
2. What do Models generally inherit from in rails?

	```
	class Name < ApplicationRecord
	```
3. What do Controllers generally inherit from in a rails project?

	```
	class NamesController < ApplicationController
	```
4. How would I create a route if I wanted to see a specific horse in my routes title assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?


	In config/routes.rb:
	```resources :horses, only: [:show]```

5. What rake task is useful when looking at routes, and what information does it give you?

	```
	rails routes
	```
	This gives you a routes table with the Prefix, Verb, URI, and Controller#Action.
	
6. What is an example of a route helper? When would you use them?

	ex: `link_to`
	
	Route helpers allow programers to write code that is more concise than HTML/erb to access other parts of the application.
	
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

	`_path` gives a route relative to the application while `_url` gives the full URL with protocol, server, and path.
	
8. What are strong params and why are they necessary?

	Strong params are parameters that can't be used in a model until they are permitted. This is important because it forces the programmer to conciously think about what attributes they are making available and acts as a double check against allowing sensitive information to become accessible. 

9. What role does `form_for` play in helping us create our forms?

	`form_for` is a Rails helper method that allows us to create a form that compiles into an HTML form.

10. How does `form_for` know where to submit the user's input?

	`form_for` knows where to submit the user's input by looking at the instance variable(s) given.
	
11. Create a form using a `form_for` helper to create a new `Horse`. 

```
<%= form_for(@horse) do |f| %>
  <p>
    <%= f.label :name %><br />
    <%= f.text_field :name %>
  </p>
  <p>
    <%= f.submit %>
  </p>
<% end %>
```
12. Why do we want to validate our models?

	We validate our models so that only valid data is saved to the database. This is important so that when data is used in later methods it does not return an error.
