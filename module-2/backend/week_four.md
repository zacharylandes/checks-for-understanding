## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
<<<<<<< HEAD
  A cookie is a bit of data that is stored on the browser that follows a user while they visit a website.

* What’s the difference between a session and a cookie?
=======

  A cookie is a bit of data that is stored on the browser that follows a user while they visit a website.

* What’s the difference between a session and a cookie?

>>>>>>> e03f2ed353d5d2be233b5022e2f172e09f8b91b1
A cookie is the data that is stored about a user usually on the browser,  a session is the data about the user that is stored on the server. Though in Rails, the session is stored on the browser so there isn't too much difference.

* What’s a flash and when do you want to use flashes?

Flashes are bits of text that are displayed to report the status of an action, usually after something has been submitted by the user

* Why do people say “HTTP is stateless”?

<<<<<<< HEAD
HTTP is statelss because it see every call as an entirely new call and doesn't store history or relationships in the call.
=======
HTTP is statelss because it sees every call as an entirely new call and doesn't store history or relationships in the call.
>>>>>>> e03f2ed353d5d2be233b5022e2f172e09f8b91b1

* What’s authentication? Explain.

Authentication is the process of making sure that the user of a site is able to see only the information that is related to that user, and not able to view
other people's information or parts of the database they shouldn't have access to.

* What’s the difference between authentication and authorization?

Authentication is verifying who is using the site, authorization is determining what permissions a user has based on their role.


* What’s a before filter?

  A before filter checks to make sure the user is allowed to see the information before showing them the info.


* How do we keep track of a user once they’ve logged in?

   The sessions controller keeps track of the user and continually verifies them.

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

<<<<<<< HEAD
nested routes are built off of resources that are dependent on each other. For example, if a user has many books, the books could be nested under the users routes.
=======
Nested routes are built off of resources that are dependent on each other. For example, if a user has many books, the books could be nested under the users routes.
>>>>>>> e03f2ed353d5d2be233b5022e2f172e09f8b91b1

  namespaced routes are more used for authorization and they tell rails to look under the folder structure defined by the routes.

  for instance,
namespace :admin do
  resources :book,
end

rails will look in an admin folder for the articles routes. This is used to separate permissions for different types of users.

* At a high level, what tools can you use to implement authorization? How would you use them?

  We use enums and roles to implement authorization. If a user has a role of 0, they are considered a default user and have no admin privileges.
  With a role of 1, they are usually considered admin. We then use sessions to verify that current users have the appropriate role.

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

Enums assign roles as an integer and this allows for faster access to authorize users. They are declared in the model.

* What are some strategies you can use to keep your views DRY?

  Avoid putting logic in the views, put logic in the models as much as possible. Use form helpers to call code that is reused and requires user input. Use Application.hmtl.erb to put code that is used everywhere on your site. Use link_to and image_tags to make use of rails helper methods/
