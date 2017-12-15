## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
<br>
rails new project_name -T -d="postgresql"
<br>

2. What do Models generally inherit from in rails?
<br>

Application record
<br>

3. What do Controllers generally inherit from in a rails project?
<br>

Application Controller
<br>

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
<br>

resources :horses, only[:show]
<br>
5. What rake task is useful when looking at routes, and what information does it give you?
<br>
rake routes, shows the path name, the verb, the url, the conroller and view associated with your routes
<br>
6. What is an example of a route helper? When would you use them?
<br>
a route helper allows you to just type in the associated path using rails conventions instead of having to write out the whole url
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  <br>
`_url` gives needs to be the whole url, `_path` only needs the prefix or path name
8. What are strong params and why are the necessary?
<br>
they are private params that are not accessible through the url
<br>

9. What role does `form_for` play in helping us create our forms?
<br>
it allows us to make forms associated to specific resources and allows us to route helpers
<br>

10. How does `form_for` know where to submit the user's input?
<br>

Because of the arguments that are passed it and also the route helper
<br>
11. Create a form using a `form_for` helper to create a new `Horse`.
<br>

<%=form_for @horse do |f|%>
<%=f.label :name%>
<%=f.text_field :name%>
<%end%>
<br>

12. Why do we want to validate our models?
<br>
So we know we are getting the appropriate information from the user
