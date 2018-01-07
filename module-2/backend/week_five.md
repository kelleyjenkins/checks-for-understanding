Questions from Week 5:
1. How do we make flash messages display on a page?
    - By using a flash notification that you set in the controller and then (typically) in your application.html.erb you would iterate through flash messages with the following syntax:
    ```ruby
        <% flash.each do |type, message| %>
          <%= content_tag :div, message.html_safe, class: type  %>
        <% end %>```

2. Where is cart information/temporary information usually stored?
    - in a session

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?
    - We don’t want to store a cart in the database because cart information changes a lot as people add and remove things from the cart. We might want the final cart information to persist in a database because then it could be transferred into an order easily.

4. What is the purpose of the asset pipeline?
    - The asset pipeline attempts to decrease the time it takes for our pages to load by speeding up the access to the static assets. By saving information in the cache there does not need to be a trip to the server to access certain files. The asset pipeline makes assets more compact, precompiles languages related to CSS/JS, and fingerprints file names to account for files changing.

5. Why do we precompile our assets?
    - Our browser understands 3 languages—HTML, CSS and JS. The asset pipeline handles the translation of sub languages like SASS, Coffeescript, etc. into CSS/JS/HTML. By storing these files in the cache they are ready to display our webpage quickly and efficiently.

6. What do each of the following tags do?
```ruby
<%= stylesheet_link_tag "application" %> -- this calls to the application.css file in yoru stylesheet folder and will compile any application files with other extensions that are kept in your stypesheet folder serve the application.css file.
<%= javascript_include_tag "application" %>-- same as above but will load all javascript files as .js
<%= image_tag "rails.png" %> -- this will compile all images in your assets > images folder
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
    -	explanation of project
    - visual representation of database
    - who created the project
    - snippets of code
    - how to get started using your app/project/gem etc.
    - how to execute the test suite
    - any special instructions necessary to use project
    - gems and special features of your project
    - Some benefits of taking the time to update a readme for a project are that users will be able to quickly implement your project, people will be able to understand your application, and employers or people interested in your project will see well organized and complete directions.  

8. What are the top four accessibility issues that we as developers should be aware of?
  - visual
  - mobility
  - cognition
  - hearing impairment

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  - before_save is an example of a callback. We would find this in the update or create methods of a resource.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
```ruby
scope :user, where(‘user.active == true)
```

11. What is the difference between a scope and a class method?
  - They achieve the same thing just have different syntax. Scopes are less error-prone and avoid the problem of nil objects

  Review Questions:  
  12. Given the following hash:  

  ```ruby
  {cart: {"17" => 4, "204" => 52, "29" => 22}}
  ```

    12a. How would you add item with id of 48 with a quantity of 4?  
    12b. How would you increase the quantity of item 29?  
    12c. How would you find out how many items your user is thinking about purchasing?   

  13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
  14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
