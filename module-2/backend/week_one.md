## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  GET: To read the information without any information being passed
  POST: To create new information
  PUT: To update a certain part of a record
  PATCH: To update the entire record
  DELETE: To destroy (or delete even) an entire record
2. What is Sinatra?
  Sinatra is a lightweight HTTP framework which allows us to build things that other people can see
4. What is MVC?
  MVC stands for Model View Controller and it is the basic file structure for web apps.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  Conventions make it easy for other people to pick up where you left off. It also makes it easy for you to pick up where past you left off.
6. What types of variables are accessible in our view templates without explicitly passing them?
  Instance variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end

  get '/horses/:id' do
    @count = Horse.find(params[:id]).count
    erb :index
  end

  get '/hello/:name' do
    name = Horse.find_by(name: params[:name])
    erb :hello, :locals => {:name => params[:name]}
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  See above
9. What's the purpose of ERB?
  ERB is a Ruby and HTML framework that allows us to render views with Ruby code included.
10. Why do I need a development AND test database?
  Loading a development database every time you wanted to run a test would slow down testing of new features. Using a test database gives us the confidence that our program is working well without having to run through the entire database every time.
11. What is CRUD and why is it important?
  CRUD stands for Create, Read, Update, and Delete. It is the four functions that a user should be able to perform on a website.
12. What does HTTP stand for?
  HyperText Transfer Protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  <% RUBY %> and <%= RUBY %>. The first does not render to the view and the second does render.
14. What's an ORM?
  Object Relational Management is a system which allows us to use SQL in object oriented programming languages.
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  ActiveRecord
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  get '/' allows us to visit the root
  get '/restaurants' allows us to view all restaurants
  post '/restaurants' allows us to create a new restaurant
  get '/restaurants/:id' allows us to view a certain restaurant
  get '/restaurants/:id/edit' allows us to edit a certain restaurant
  put '/restaurants/:id' performs the edit on a certain restaurant
  delete '/restaurants/:id' destroys a certain restaurant
17. What's a migration?
  Migration creates new tables in the database
18. When you create a migration, does it automatically modify your database?
  No, you have to run the migration
19. How does a model relate to a database?
  The model is the object that allows us to interact with the database
20. What is the difference between `#new` and `#create`?
  #new doesn't save the record, it just creates a record ready to be saved. Create creates the record and saves it in one command

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
  ```ruby
  CSV.foreach("./db/csv/films.csv", OPTIONS) do |row|
    Film.create!(row.to_hash)
  end
  ```
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
  ```ruby
  activities[brunch][supplies] << 'granola bar'
  ```
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  Encapsulation : This is the principle that defines scope.
  Abstraction : This is the principle that everything should only know what it needs to know.
  Inheritance : This means that classes can inherit methods from classes above them.
  Polymorphism : This means that a variable can only hold one value but can be changed.


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
