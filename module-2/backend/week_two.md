## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
<br>
  Active record is a translation tool for writing SQL. It simplifies a lot of the long SQL commands and turns it into SQL for the computer to read.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

Because team inherits from Active Record you can use the active record methods like:
 where, find,order, and group

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

team = Team.find(:id => 4)
Owner.find(:id => team.owner_id )

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

team = Team.find(:id => 4)
team.owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Teachers have_many students
and a student belongs_to a teacher

in the schema, students will have a foreign key of teacher_id

6. Define foreign key, primary key, and schema.
a foreign key is the column that  two tables share together to bind them together.
a primary key is a unique column in a database, and usually pertains to a single table
 a schema is the visual representation of the database

7. Describe the relationship between a foreign key on one table and a primary key on another table.

A foreign key on one table refers to the primary key on another table, the teacher_id column is the foreign key on the students table , which refers to the primary key, id, on the teachers table.

8. What are the parts of an HTTP response?

head and body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?

Teachers have_many students
and a student belongs_to a teacher

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?


6. Give an example of when you might want to store information besides ids on a join table.

7. Describe and diagram the relationship between patients and doctors.

8. Describe and diagram the relationship between museums and original_paintings.

9. What could you see in your code that would make you think you might want to create a partial?
if you see a lot of repetitive html code
