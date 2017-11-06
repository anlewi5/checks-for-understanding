1. How do we make flash messages display on a page?

	```flash[:something] = "message to display"```

	Then in application.html.erb:
	
	```ruby
	<% flash.each do |type, message| %>
 	 <%= content_tag :div, message, class: type %>
	<% end %>
	```

2. Where is cart information/temporary information usually stored?

	In a session.

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?

	We probably don't want to store cart information in the database because it takes up more storage space.
	
	We might want to persist cart information so that a user can log out without checking out and then log back in later and still have the items they want in their cart.

4. What is the purpose of the asset pipeline?

	The asset pipeline's purpose is to prepare JS, CSS and images for the browser to read. It does this through (1) precompiling, (2) concatenation, and (3) minification.

5. Why do we precompile our assets?

	We precompile our assests so that they are in the language that the browser reads.

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

	These helper tags format what is put into them as HTML code.

COME BACK

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

	Elements of a great ReadME:
	1. tells how to spin up the application from an "I know nothing" point of view
	2. gives information about languages and frameworks used
	3. uses clear language and doesn't make assumptions about what the person reading it should or shouldn't know

	Benefits:
	1. provides guidelines for you code (ReadMe Driven Development)
	2. if in a group, clarifys the groups main goals

8. What are the top four accessibility issues that we as developers should be aware of?

	1. vision
	2. cognative
	3. mobility
	4. hearing

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

	`before_save` is an example of a callback. We might find it used to generate a slug.

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```

	In the User model:
	
	`scope :active, => { where(active: true) }`

11. What is the difference between a scope and a class method?

	The two are the same, the difference lies in the syntax. The above could also be written as:
	
	```ruby
  	def self.active
    	where(active: true)
  	end
  	```
