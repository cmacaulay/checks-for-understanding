## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What is Webpack and why is it useful?
Webpack is a node package that works similarly to a bundler in your Rails app. It is going to scan your project and locate any dependancies you might have, and will make sure that these are included and "bundled" into your final product - generally compiling a number of files (JS, Stylesheets) into one neat one. It bridges the gap between your (static?) files and what the browser can interpret.
2. When do you want to use event delegation?
When you want events to happen in a specific order by avoiding new event listeners and instead passing events between each other.
3. What's one difference between ES5 and ES6?
Arrow functions! =>
4. What's the deal with semi-colons in JavaScript?
Totally optional, personal preference thing, although a lot of people do use them. They go at the end of of statement. Whether you use them or not, you should have a reason for it. If you put them in the wrong place you can confuse your browser.
5. How are you using the MVC design pattern in your Quantified Self project?
Model - Similar to models in a Rails app, we have built out model classes in Node for our Quantified Self back end.
Views - Our separate front-end is acting as the View portion of the MVC pattern, utilizing AJAX calls to connect the front-end to the back-end.
Controllers - While we have built controllers in our back end, I feel like the server.js, router files and controller files are all kind of jointly doing the same jobs that controllers and routes would do in a rails app. The boundaries of responsibility seem less clear when working with express.
6. How do you execute raw SQL in node?
When using the KNEX library, you are able to call knex.raw if it's helping build your database, and database.raw when you're interacting with your database. Without knex, I'm guessing there are some psql commands you can use to use raw SQL in your app.
7. What is CORS?
It's rude! It is an automatic setting that protects data endpoints from external access unless specified.
8. What are some steps to avoid CORS?
Adding headers to your HTTP response that allow access.

#### Review  

9. Why do people say "HTTP is stateless"?
Each request/response cycle is independent, the connection between the client-side and the server ends once the request/response ends, meaning no data is stored. That's why we need sessions & cookies.
10. What is a RESTful API?
It is an Application program interface (API) that follows RESTful convention and GET, PUT, POST and DELETE HTTP requests.
11. What are some main characteristics of a team following an agile workflow?
Breaking down the challenge into small parts, and focusing on iterating the project in small chunks so as to be flexible and make changes on the go vs. try to accomplish a big thing at first (waterfall).
12. What are some advantages/disadvantages to using OAuth to authenticate a user?
Advantages: A lot of security concerns are taken care of for you, the user does not have to remember another user log in.
Disadvantages: Sometimes the OAuth APIs are tough to work with, you're reliant on there not being a bug in someone else's code.
