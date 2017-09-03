## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
AR is a Object Relational Mapper. It allows us to store and query items from a database and turn them into objects which we can then call methods on.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

You can call things like .all, .count, .find, .find_by etc. They are all active record methods, which are avaialble because the class inherits from ActiveRecord::Base.


3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

Team.find(4)

Owner.find(Team.find(4).owner_id)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

Team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Teacher
has_many :students, through: student_teachers

Student_Teacher
belongs_to: student
belongs_to: teacher

Students
has_many :teachers, throughL student_teachers

6. Define foreign key, primary key, and schema.
Primary key is the unique number given to every entry in a dtabase table. Foreign key is a key relating to a primary key on another table. Schema is the layout of all columns on all tables. It shows what information is where and what relationships exist between tables

7. Describe the relationship between a foreign key on one table and a primary key on another table.

They are the same number and used to relate the two pieces of information that lie in either table.

8. What are the parts of an HTTP response?

The head and the body.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
.pluck - pulls out all the entries from one column of the table
.group - based on what comes before it, it returns a hash of grouped items from the table. Useful for counting multiple              cases
.find_or_create_by - either finds the record or creates a new one if it doesn't exist
.joins - creates a join table
.order - sorts records in asc or desc order by a particular column

2. Name your three favorite ActiveRecord rake tasks and describe what they do.

db:rollback - rollsback a migration, can take an argument to rollback multiple
db:migrate:reset - drops all tables and re-runs migrations
db:seed - puts in the data i.e. runs the seed file

3. What two columns does `t.timestamps null: false` create in our database?

created_at
updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

You asked this question already.

6. Give an example of when you might want to store information besides ids on a join table.

In the teachers students example, on the student_teacher joins table, you may want to include information like which class the teacher and the student are joined on.

7. Describe and diagram the relationship between patients and doctors.

A doctor has many patients. A patient has one doctor.

8. Describe and diagram the relationship between museums and original_paintings.

A musuem has many original_paintings. An original painting belongs to a museum

9. What could you see in your code that would make you think you might want to create a partial?

The need to display an error message for improper input.
