## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
ActiveRecord is a library of methods that allows developers to use ruby to interact with the database. This is possible because the ActiveRecord methods are writing the sequel for us. 
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
maximum
average
group
find_or_create_by
where
order
uniq
pluck
joins
=> through Activerecord. 
3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
team = Team.where(id: 4)
team.name 
=> "Team Name"
team.owner_id.pluck(:name)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```
Now how would you find the owner of the team with an id of 4?
team.owner.name

<<<<<<< HEAD
5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
6. Define foreign key, primary key, and schema.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
8. What are the parts of an HTTP response?

=======
3. What do they allow you to do?
Call on the singular of that column and have access to its attributes. 
7. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Posting load code in a comment.
8. Define foreign key, primary key, and schema.
Schema - This holds the basic structure of your data-base. Migrations determine the makeup of the schema. Where tables live. 
Primary Key - Unique identifier that every record is created with. 
Foreign key - Link to another table through the unique identifier of a specific record in the second table. 
9. Describe the relationship between a foreign key on one table and a primary key on another table.
They are the same? 
10. What are the parts of an HTTP response?
Client --> Request --> Routes --> Controller --> Model --> Database
Database --> Model --> Controller --> Response/View --> Client
11. Describe some techniques to make our Sinatra code more DRY. Give an example of when you would use these techniques.
- Using partials for the edit and new views. 
>>>>>>> 8d08c119345e078a951f8902205d19d5ab9030ce

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
<<<<<<< HEAD
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
=======
rake db:reset - just kidding! 
rake db:test:prepare because, testing! They make sure your test environment has been updated with any new migrations. 

4. What can you expect from a group as you begin working together? As you continue working together?
Storming & Norming. 
5. What two columns does `t.timestamps null: false` create in our database?
6. What cURL flag can you use to send a `POST` request?
7. What case does JSON (and JavaScript) use for multi-word variables?
8. What case does Ruby use for multi-word variables?
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
11. Give an example of when you might want to store information besides ids on a join table.
12. Describe and diagram the relationship between patients and doctors.
13. Describe and diagram the relationship between museums and original_paintings.
14. What are some examples of acceptable values for the parts of an HTTP response?
15. What types of output do we want to test when we test our controllers?
16. What could you see in your code that would make you think you might want to create a partial?
17. Why might you use a helper method?
>>>>>>> 8d08c119345e078a951f8902205d19d5ab9030ce
