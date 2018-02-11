## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?

rails new <name_of_project>

2. What do Models generally inherit from in rails?

ApplicationRecord

3. What do Controllers generally inherit from in a rails project?

ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

resources :horse, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?

rails routes, it gives you path prefixes, the URIs, and the method

6. What is an example of a route helper? When would you use them?

edit_movie_path(movie). You use them to not have to write out the URI every time

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

`_url` returns the entire URL and `_path` returns the URI

8. What are strong params and why are they necessary?

Strong params check for permitted attributes before sending them back to be created or updated

9. What role does `form_for` play in helping us create our forms?

`form_for` allows us to create forms that can be re-used throughout the folder.

10. How does `form_for` know where to submit the user's input?

`form_for` takes an argument from a variable to determine what to do.

11. Create a form using a `form_for` helper to create a new `Horse`.

`<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
<% end %>`

12. Why do we want to validate our models?

We want to validate our models to ensure that information is not put into our database that isn't what we want it to be.

13. What are the steps of the DNS lookup?

It looks locally first, then to your ISP, then to your top-level domain lookup, and finally to the registrars.

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?

move.prance

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  

`furniture[table][purchased]` for true and `furniture[table][height]` for 3

16. What is inheritance?

It changes the superclass of an class.

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel overwhelmed by the content presented this week
