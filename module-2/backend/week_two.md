## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  
  ActiveRecord is a Opject Relational Mapper that allows you to use built in methods that help turn databases into objects when using Rails. It allows us to manipulate data with ActiveRecord methods and Ruby. 
  
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  
  Some methods you can call on Team might be order, group, join, group_by, find_by, find... We have access to these methods because the class Team inherits from ActiveRecord allowing Team to use any methods that ActiveRecord has. 

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
  ```name = Team.find(4).name```
  ```owner =Team.find(4).owner_id```

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  
  ```Team.find(4).owner```
    

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  
  
  Teacher has_many Sudents
  Student belongs_to Teacher
  
  Student:
  - name
  - teacher_id
  
  Teacher:
  - name
  
  
6. Define foreign key, primary key, and schema.
  
  - Schema- teh schema is the result of a migration which shows you how the migration is displaying information from the actual database.
  - Primary Key- The primary key is the column in a table that identifies each entry uniquely-- often is an id. 
  - Foreign Key- The foregin key is the column you are matching your tables by. 
  
7. Describe the relationship between a foreign key on one table and a primary key on another table.
    
    The foreign key on one table matches a primary key on the other table and it is what links the two database. For example, a Student belongs to a Teacher, there would be a teacher_id in the Student database and that teacher_id is the foreign key because it matches an individual teacher in the Teacher database.

8. What are the parts of an HTTP response?

  - Status line - includes HTTP version that matches the request and status code (error, success, etc)
  - Header - key/value pair
  - Body- contains information requested
  

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
