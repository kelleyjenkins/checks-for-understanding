## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
  * GET- pulling a resource from database
  * POST - creating a resource in a database
  * PUT - updating a resource
  * PATCH - updating part of a resource
  * DELETE - deleting a resource

2. What is Sinatra?

    Sinatra is a domain specific language that uses MVC. 

4. What is MVC?

    MVC stands for Model, View, Controller and is convention used for displaying web pages in Rails and Sinatra

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

    Because it allows for Restful routes which create a common way to identify and follow the structure of the app.

6. What types of variables are accessible in our view templates without explicitly passing them?

    Variables that we create in our controller are accessible to view templates. 

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```
    In index view you would call horses.count

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

    in controller define:
    
    name = "Mr. Ed"
    
    in index call horse.name 

9. What's the purpose of ERB?
  
  ERB is an embedded ruby file where you can use html to display your app but within the html, you can use ruby logic to get the results you want to output to the screen. 
  
10. Why do I need a development AND test database?
    
    IDK

11. What is CRUD and why is it important?

  CRUD stands for create, read, update, delete and it is important because we must be able to create resources for our databases, read them, update or edit them, and delete them. 
  
12. What does HTTP stand for? 
  
  Hypertext Transfer Protocol 
  
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  
  <%= %> using this tag will display your Ruby output in the view.
  
  <% %> and using this tag will perform the logic but not display it to the page. 
  
14. What's an ORM?

  Object Relational Mapping- 

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  
   ActiveRecord

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
   
  * get '/root' do -- this will retreive the page with the root you are starting at
  * get '/root/new' do -- this will retreive the page with a form to enter the new resource 
  * post '/root' do -- this will actually create the new resource and add it to the database
  * get '/root/:id' do -- this will access a single resource
  * get '/root/:id/edit' do -- this will access the form page to edit your resource
  * put 'root'/:id do |id| -- this will update the resource id you edited
  * delete 'root/:id' do |id| -- this will delete the record you chose

17. What's a migration? 
  
  A migration is a way to create tables and databases in ActiveRecord

18. When you create a migration, does it automatically modify your database?
  
  Creating a migration simply gives your table a name. You must also fill in the instructions for your table in the migration file and perform the migrate command (rake db:migrate) to actually migrate the data into the table. 

19. How does a model relate to a database?
   
   The model allows you to call methods on attributes you've established in your database.

20. What is the difference between `#new` and `#create`?
  
  .new will create a new object as specified but it will not save it to your database. .create will both create the object and save it into your database in one sweep. 

Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

    First I'd run rake db:create_migration NAME=create_films in the terminal. Then in the file that is created I would add to the change method
    
```create_table :films do |film|
    film.integer :id
    film.text :title
    film.text :description```
    
 Once that was complete, I would run rake db:migrate to load the data as specified. 
  
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores'] 
}
```
How would I add 'granola bar' to things you should have when hiking? 

  ``` activities[:hiking][:supplies] << "granola bar" ```

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  * Abstraction - simplifying a complex action with a verb
  * Encapsulation - keeping as much state and logic within class
  * Inheritance - ability for classes to inherit behaviors and attributes from parent classes
  * Polymorphism - something that occurs in many forms
