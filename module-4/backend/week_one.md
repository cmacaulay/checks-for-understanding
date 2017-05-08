## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
How to think through problems in a new language. 
2. What are some tools to help debug JavaScript code?
Pry, debugger, error messages, linters. 
3. What are some tools you need in order to unit test your JavaScript?
Mocha, chai, exporting. 
4. What is the syntax for invoking a function?
name()
5. What's the difference between `==` and `===` in JavaScript?
'===' is a strict equals, which means the values need to math both in value and data type. '==' would accept like values of different data types, e.g. 3 == '3' would evaluate true, while only 3 === 3 would do the same. 
6. What's the difference between asynchronous and synchronous JavaScript? 
Asqnchronouls JS is the impatient of the two, there's no order to what's loaded, everything loads independantly regardless of how slow something else might be. 
7. What's a callback function and what are some reasons when we use/need callback functions?
It's when you nest functions within eachother in order to dictate an order they're executed in. 
8. What's the biggest difference between a promise and a callback?
The ability to give exceptions - e.g. error() or catch().
9. How do we setup a route when creating an API with Node and Express?
```
app.get('/', function (request, response) {
  response.send('Testing')
})
```
10. What's `npm` and what do we use it for?
node package manager (?), we use it similarly to how bundle handled ruby gems. It is an easy way to install external libraries or other plug-ins.  

#### Review  
11. What's the MVC design pattern? Describe each part of MVC?
Model - Defines the object attributes and methods for each table
View - What's rendered client-side
Controller - air traffic controller, routes the requests to render the correct view, retrieving information from the database that's filtered through the rules in the model. 
12. What is AJAX? What are some benefits of using AJAX?
jquery requests that can retrieve data client side. Often fast at retrieving data. 
13. What's a background worker? When would we want to use a background worker?
A background worker executes a script behind the scenes, you might want to use one to maintain up to date information. 
