## Week Two - Module 3

Some of these questions are from this week, some are from previous weeks, and some are new concepts. Try answering without research first. If you are not sure, take a guess but acknowledge that it's a guess (faking an answer in an interview without acknowledging it as a guess is a bad idea). Follow up with the necessary research to understand these concepts. These tend to be common themes during the job hunt and are worth having a solid understanding of.

1. What's OAuth?
 - The authentication for your app is taken care of by that provider and you can use the information received from the provider. 
1. What are some advantages/disadvantages of implementing OAuth?
  - Your app has access to all the information that the provider has already received from the user. Disadvantage is it's difficult to obtain additional information from user. Another disadvantage is that the user must have an account w/ the provider in order to use your app.
1. What are the four pillars of object oriented design? 
 - Abstraction
 - Inheritance
 - Encapsulation
 - Polymorphism
 How do they apply when creating:
  * services? Services are a way to organize more complex logic. It abstracts your method so there is less in controller. 
  * PORO's with the data received from an API?   
1. What do we use VCR for? Why is it a good idea to use this tool?
 - VCR is a way to avoid making excessive API calls when testing your app. It records your initial API call and refers to that recording for future tests. It is a great way to test however it will not pick up changes that are made by your API. Need to delete cassettes in order to receive new infomation from the API call.
1. What does HTTP stand for?
- Hypertext Transfer Protocol
1. What class does `ApplicationController` inherit from when creating a Rails project with the `--api` flag? What about without the `--api` flag?
- ActionController::API with --api flag vs ActionController::Base without --api flag
  * What is `protects_from_forgery`?
   - You send out a request with a token so that your responses are specific to you. 
  * What do you need to do differently for your API to accept non-GET requests if you did not use the --api flag?
1. How do you create the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age) 
   CREATE TABLE users (first_name:string, last_name:string, email:string, age:integer)
   rails g migration CreateUsers first_name, last_name, eamil, age:integer
1. What does `inject` do? How should you use it?
- inject = reduce and should be used when you are trying to return a single object. 
#### Self Assessment  
Rate yourself on the following scale.  
4 I know and understand all these concepts and did not have to look anything up  
3 I know and understand most of these concepts but had to look something up  
2 I am uncertain about some of these concepts and had to look some things up ^^  
1 I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up.
