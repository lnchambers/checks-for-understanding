## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

ActiveRecord is the Model part of MVC. It allows you to inherit methods to manipulate the data from ActiveRecord to make your models function as expected

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

.average, .find, .find_by, .order, .where. You have access to these methods through inheriting ActiveRecord::Base

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

team = Team.find(4).name

Owner.find(team.owner_id)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

Owner.find(team.owner_id)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

In the case of Turing, it would be a one to many relationship. A student would belong to a teacher and a teacher would have many students. A student would have a teacher_id foreign key column.

6. Define foreign key, primary key, and schema.

A foreign key is an id relating to another table, a primary key is the organization of a single table, and a schema is a visual representation of the entire database.

7. Describe the relationship between a foreign key on one table and a primary key on another table.

A foreign key on one table is the primary key on another table.

8. What are the parts of an HTTP response?

A status line, a header, and a body.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.

.maximum : Returns the highest value of the column in the argument
.where : Returns all instances of the supplied argument.
.average : Returns the average of all values in the column.
.order : Returns the column selected ordered in lowest to highest order.
.find : Returns the first instance in the column that matches the argument.

2. Name your three favorite ActiveRecord rake tasks and describe what they do.

3. What two columns does `t.timestamps null: false` create in our database?

created_at and updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?

A teacher would belong to a school and a school has many teachers.

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

You would need to put the school primary key in the teacher's table.

6. Give an example of when you might want to store information besides ids on a join table.

Data that only applies when the two data sets are joined.

7. Describe and diagram the relationship between patients and doctors.

A patient has many doctors and a doctor has many patients. You will need a join table to match them together.

8. Describe and diagram the relationship between museums and original_paintings.

A museum has many original_paintings and an original_painting belongs to a museum.

9. What could you see in your code that would make you think you might want to create a partial?

When you are repeating yourself in HTML. A nav bar or something that is repeated on every page would need a partial.
