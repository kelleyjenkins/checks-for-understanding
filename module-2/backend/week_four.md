## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
* What’s the difference between a session and a cookie?
* What’s a flash and when do you want to use flashes?
* Why do people say “HTTP is stateless”?
* What’s authentication? Explain.
  Authentication is identifying that the user is who they say they are for security purposes and to ensure that the user has access to what they should have access to. 
* What’s the difference between authentication and authorization?
  Authentication verifies the identity of the user, while authorization permits that user to see/do certain things in the app. Authentication is that a user is who they say they are and authroization is that a user can do see what they should see. 
* What’s a before filter?
 A before filter is a way to instruct the controller to do a specific action before performing any or certain methods within that controller. For example, a before_action :require_admin would cause the app to check that the current user is an admin before performing the actions in the controller. 
* How do we keep track of a user once they’ve logged in?
  Sessions help us keep track of a user once they've logged in. 
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
* At a high level, what tools can you use to implement authorization? How would you use them?
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
* What are some strategies you can use to keep your views DRY?
