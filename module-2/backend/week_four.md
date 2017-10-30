## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?

	Cookies are key-value pairs stored in a user's browser (client-side) that act like 'bookmarks'
	
* What’s the difference between a session and a cookie?

	Sessions are entire hashes stored in a *secure* cookie.
	
* What’s a flash and when do you want to use flashes?

	Flashes are 'hashes' that persist from 1 method to the next and are useful in communicating 1-time messages to users such as 'successful login.'
	
* Why do people say “HTTP is stateless”?

	HTTP doesn't store information from one request to the next: each request-response is independant from another.
	
* What’s authentication? Explain.

	Authentication is ensuring that the user is who they say they are.
	
* What’s the difference between authentication and authorization?

	Authentication is *who* the user is, authorization is *what* the user is allowed access to.
	
* What’s a before filter?

	A before filter contains code to be run before other methods in the controller.
	
* How do we keep track of a user once they’ve logged in?

	We keep track of a logged in user through a session hash.
	
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

	Nesting a resource makes the resource accesible only through the resource in which it is nested, generating a different path than it would otherwise have. Namespacing allows grouping of controllers, which provides organization.
	
* At a high level, what tools can you use to implement authorization? How would you use them?

	1. `allow_any_instance_of` 'fakes' a user login for the purposes of testing.
	2. Enums allow us to rename numbers to more understandable words, this helps in assigning roles such as "admin" and "user" instead of 1 and 0. Enums also give us additional methods which we can use in testing and determining the roles of users.
	3. Namespacing helps us organize our different roles.
	4. `before_action` allows us to apply methods prior to running actions in our controllers, such as checking to see if a user is logged in before allowing them access to a page.
	5. Inheritance allows us to refactor our code.

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

	Enum is a method which allows us to 'rename' integers from our database as whatever we want(hopefully something more understandable). Enums are declared within our controller.
	
* What are some strategies you can use to keep your views DRY?

	1. Partials
	2. Shared and Application (folders)
	3. Removing actual code and placing it in the models
	4. Using rails helper methods
