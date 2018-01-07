1. How do we make flash messages display on a page?

  by putting this code in application.html-
      <% flash.each do |type, message| %>
      <%= content_tag :div, message.html_safe, class: type %>
    <% end %>
  and then calling the message in the controllers.

2. Where is cart information/temporary information usually stored?
<br>

as a hash in a PORO

<br>
3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?
<br>

We don't want it in our database because users don't have to be authenticated to have carts, we want our database to only have secure info. We could want to persist that info if the user is authenticated and we want to save their info upon login.
<br>

4. What is the purpose of the asset pipeline?
<br>

it speeds up the loading of our assets, like JS, CSS, and HTML.
<br>

5. Why do we precompile our assets?
<br>

we precompile to make our files readable faster to servers and browsers.

<br>


6. What do each of the following tags do?
<br>


<%= stylesheet_link_tag "application" %>
<br>
this finds the all the stylesheets in the app
<br>

<%= javascript_include_tag "application" %>
<br>
this finds all the js in theapp
<br>


<%= image_tag "rails.png" %>

<br>
this renders rails.png
<br>


7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
<br>

a good readme should have context and be very clear and readable to anyone.
<br>

8. What are the top four accessibility issues that we as developers should be aware of?
<br>
Visual
mobility
cognition

<br>


9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
<br>
this is a callback,
we would find it in the base controller
<br>
10. Given the following object, how would we create a scope for all users who are active?
<br>
```ruby
User.create(name: "Happy", active: true)
```
  scope :true, -> { where(active: 'true') }

<br>
11. What is the difference between a scope and a class method?
<br>
Internally they are the same, but visually, scoping is cleaner.

the above would look like below as a class method.
<br>
def self.true
  where(active: 'true')
end
