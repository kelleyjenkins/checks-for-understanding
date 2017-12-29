## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
  - A cookie is an identification tool that stores a small peice of data in the browser of a website. It is always stored on the client side. 
* What’s the difference between a session and a cookie?
  - A session typically lives on the server (but not with Rails), and it is used to track a specific cookie. It can store small amounts of data that will persist between requests. 
* What’s a flash and when do you want to use flashes?
  - A flash is a special part of a session that is cleared wth each request, so if a person logs out the session and information is destroyed forcing user to log in again next time they visit that site. 
* Why do people say “HTTP is stateless”?
  - HTTP is stateless because websites do not by default remember anything a user inputs without use of a cookie/session. By using sessions you make the HTTP stateful and capable of remembering information. 
* What’s authentication? Explain.
  - Authentication is identifying that the user is who they say they are for security purposes and to ensure that the user has access to what they should have access to. 
* What’s the difference between authentication and authorization?
  - Authentication verifies the identity of the user, while authorization permits that user to see/do certain things in the app. Authentication is that a user is who they say they are and authorization is that a user can do see what they should see. 
* What’s a before filter?
 - A before filter is a way to instruct the controller to do a specific action before performing any or certain methods within that controller. For example, a before_action :require_admin would cause the app to check that the current user is an admin before performing the actions in the controller. 
* How do we keep track of a user once they’ve logged in?
 - Sessions help us keep track of a user once they've logged in. 
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  - Namespacing is helpful when you have routes for a specific resource but want to make sure certain users have additional functionality and control over some of those routes. For example and admin may have edit and delete functionality but you don't want all users to have that functionality. Namespacing would allow an admin route to perform those funcitons. Nesting resources is a way to capture a resources relationship within routing. If one resource is dependent on another, you might nest the resources since you can't access one resource without the other. The difference between these two approaces mainly has to do with accessability. Nesting does not restrict the views or functionality of the app for specific users while namespacing does have that ability. 
* At a high level, what tools can you use to implement authorization? How would you use them?
  - Namespacing, enums and uniqueness validations are all used to implement authorization. Namespacing provides a route specific to the namespace allowing only specific users access to certain functionality in an app. An enums attribute is an integer that defines an attribute. It's often used for frequently changed attributes like roles that might change frequently depending on the user. Uniqueness validations make it so that a when a user creates an account their username must be unique so you don't end up with 2 users with the same username. This allows the app to validate that the user is who they say they are. 
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  - An enum is a way to define an attribute using numbers. It allows your app to identify the role of a user quickly especially if roles are changing frequently. You declare an enum in the model by defining the enum with an array. An integer datatype needs to be in your database in order to use an enum. 
* What are some strategies you can use to keep your views DRY?
  - You can use form helpers and route helpers. Form helpers allow you to create one form and call that form from each of your views that require a form. Route helpers make it easier to link to different routes from your view. 
