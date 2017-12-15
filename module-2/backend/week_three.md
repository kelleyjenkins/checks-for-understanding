## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app? 
     - ```rails new```
2. What do Models generally inherit from in rails?
    - ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
    - ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
    - ```'get /horse/:id' horse#show```
5. What rake task is useful when looking at routes, and what information does it give you?
    - rake routes -- this gives you a table including the path name, route url, and http verb.
6. What is an example of a route helper? When would you use them?
    - route helper is used in place of the url when redirecting to a specific route or referring to a specific route. An example would be horses_path which would link to the index page of listing all the horses. The url would be /horses.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
    - `_url` will return the entire url whereas `_path` will return only the URI
8. What are strong params and why are the necessary?
   - strong params are used for security purposes and make it so you have to allow certain parameters to be added, updated using a form. If the parameter isn't allowed, it can't be accessed by outside user. (?? I know what these are in my app but not how to explain them!!)
9. What role does `form_for` play in helping us create our forms?
    - `form_for` allows us to create forms easily and can help keep our code DRY by allowing us to render the form in different locations. It uses strong params to allow for updates. 
10. How does `form_for` know where to submit the user's input?
    - when your create a `form_for` you pass in the instance that you are creating the form for. Based on the instance, it knows to submit the form to that instances post method. 
11. Create a form using a `form_for` helper to create a new `Horse`. 

  ```<% form_for @horse do |f| %>
        <%= f.label :name %> 
        <%= f.text_area :name %>
        <%= f.label :breed %>
        <%= f.text_area :breed %>
     <% end %>```
     
12. Why do we want to validate our models?
  - Validating our models makes it so the entries added to the database include what we need it to inlcude. Validating the presence of an attribute means it will not accept an entry that does not include that attribute. 

