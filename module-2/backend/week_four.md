## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?

A cookie is essentially an ID card stored on the client to allow for persisted state in browsing sessions

2. What’s the difference between a session and a cookie?

A session can be stored client side or server side. With Rails, the default storage is the client side. The session is contains keys to look up information from the database, the cookie is the key to a specific session.

3. What’s a flash and when do you want to use flashes?

A flash is a message that can appear in response to something being done. You want to use flashes when there is interaction on your website that would be confusing without a response.

4. Why do people say “HTTP is stateless”?

HTTP doesn't store any information. It is only responsible for sending information between the client and the server.

5. What’s authentication? Explain.

Authentication is verifying a user is who they say they are. Authentication allows for a user to maintain a presence on a website that is uniquely tied to them

6. What’s the difference between authentication and authorization?

Authentication verifies that a user is who they say they are, authorization is what that user can do once we know they are who they say they are.

7. What’s a before filter?

A before filter runs methods before running the CRUD methods. It can be scoped down to only include certain CRUD methods.

8. How do we keep track of a user once they’ve logged in?

We use a session to match that user to their information

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

You want to namespace a resource if you do not need any functionality for the namespace but it makes sense to keep it under that name. An example is admin/dashboard. A nested resource is useful when two resources are tied together inextricably. One resource that only makes sense in the context of another resource should be nested. An example of this is /users/1/user-owned-items/

10. At a high level, what tools can you use to implement authorization? How would you use them?

You can hand roll authorization or you can use gems such as OmniAuth or AuthO. You use the gems by reading the documentation and frustratingly building the functionality into your project.

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

An enum iterates through an array to assign strings based on integer index. The data type it uses is an integer, since it finds by integer index. You declare an enum in the model.

12. What are some strategies you can use to keep your views DRY?

Building cross site similar functionality in the layout html file and using partials for resource specific views.


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

After fixing the syntax error --
```ruby
array.sort_by do |hash|
  hash[:holiday][:name]
end
```
Really bad naming convention, but I wanted to illustrate the data types =)

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?

data.to_i


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel comfortable with the content presented this week
