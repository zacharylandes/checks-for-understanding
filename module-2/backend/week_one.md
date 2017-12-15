## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
  -Get- access an existing website
  -Post- create a resource from a form or URL on the server
  -Put- update a resource on the server
  -Delete - delete a resource on the server
  -Patch  - update a smaller piece of a resource on the server
2. What is Sinatra?
  -A web framework that helps in the creation of web applications in Ruby
4. What is MVC?
  -The Model,View,Controller system for structuring files in web frameworks
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  -We follow RESTful conventions so that our code is understandable to others and to create an understood structure for routing
6. What types of variables are accessible in our view templates without explicitly passing them?  
  class variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
   :locals => {:name => 'Mr. Ed'}
9. What's the purpose of ERB?
  -To allow us to perform ruby actions in the view
10. Why do I need a development AND test database?
    -to appropriately manage and keep track of data in different environments
11. What is CRUD and why is it important?
  Create, Read, Update, delete
  These are the basic actions that users perform in web applications
12. What does HTTP stand for?
  Hyper Text transfer protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  1. <%=ruby_here%>- This prints to the screen
  2.<%ruby_here%>-this performs ruby without printing

14. What's an ORM?
  -Object relational mapper, lets us speak SQL without actually using SQL
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  -Active Record
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

  get '/restaurants'-shows all restaurants
  get '/restaurants/:id'-shows individual restaurant
  get 'restaurants/new'- shows restaurant creation page
  post 'restaurants/new'- saves new restaurant to server
  get 'restaurants/edit'- shows edit page
  put 'restaurants/edit'- saves edited restaurant
  delete 'restaurant/:id'- deletes restaurant  

17. What's a migration?
  -a blueprint for a new table in the db

18. When you create a migration, does it automatically modify your database?
  -no
  
19. How does a model relate to a database?
  -models are tables in the db
20. What is the difference between `#new` and `#create`?
    'new' makes a new resource but doesn't save it
    'create' makes a new resource and saves it
Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

films = CSV.open './db/csv/films.csv', headers:true, header_converters: :symbol
films.each do |row|
  Film.create!(id: row[:id], title: row[:title], description: row[:description])
end

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

 activities[:hiking][:supplies].push('granola bar')

