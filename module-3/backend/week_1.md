## Week One - Module 3

Some of these questions are from this week, some are from previous weeks, and some are new concepts. Try answering without research first. If you are not sure, take a guess but acknowledge that it's a guess (faking an answer in an interview without acknowledging it as a guess is a bad idea). Follow up with the necessary research to understand these concepts. These tend to be common themes during the job hunt and are worth having a solid understanding of.

1. What is `json`, what does it stand for, and why is it important?

  JavaScript Object Notation: Common currency between multiple languages/frameworks; Allows splitting between backend/frontend; Allows data sharing

1. What kind of object is JSON in Ruby? How do we know it's JSON?

  In Ruby, JSON is a string that when parsed into Ruby becomes a hash or an array of hashes

1. What's an API?

  Application Programming Interface: Connection between application and program (transferrable data)

1. What's a RESTful API? How does that look in Rails?

  API falling under RESTful architecture(REpresentational State Transfer): namespacing, nesting, predictable URI paths

1. What is an ORM, what does it stand for, and why is it helpful?

  Object Relational Mapper: Abstraction above the database level, standardizes data

1. How do you create a record in the following table in SQL? In Active Record?

  ```
  INSERT INTO users VALUES ('anna', 'lewis', 'a@mail', 5);
  ```
  ```
  User.create(first_name: 'anna', ...)
  ```

   (Users table with columns first_name, last_name, email, and age)
1. How would you refactor this method?

```
def people_with_brown_hair
  people_with_brown_hair = []

  people.each do |person|
    if person.hair_color == "brown"
      people_with_brown_hair << person
    end
  end

  people_with_brown_hair
end
```
Refactored:
```
def people_with_brown_hair

  people.select do |person|
    person.hair_color == "brown"
  end

end
```

1. Given an array numbers = [1,2,3,4,5], find the sum of the doubles of all the numbers.  

```
numbers.sum * 2
```

#### Self Assessment  
Rate yourself on the following scale.  
-> 4  I know and understand all these concepts and did not have to look anything up  
3  I know and understand most of these concepts but had to look something up  
2  I am uncertain about some of these concepts and had to look some things up ^^  
1  I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up.
