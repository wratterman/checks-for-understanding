## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6?
  - String interpolation
  - Class
    - Contstructor setup  
2. What's the difference between asynchronous and synchronous JavaScript?
  - Synchronous evaluates line - line in a linear way
  - Asynchronous doesn't do that ^^
3. What are the four pillars of Object Oriented programming?
  - Abstraction
  - Encapsulation
  - Inheritance
  - Polymorphism 
4. What are some tools available in JavaScript to help you write object oriented code?
  - Constructor functions
  - JS {} objects
  - A good attitude
5. What are some key concepts to be aware of when refactoring your JavaScript?
  - What "this" is at any given time
6. What's a callback function and what are some reasons when we use/need callback functions?
  - A callback function is a function that isn't invoked unless a different function has been invoked.
7. What's the scope of variables in Javascript?
  - Global || Local
8. What's the difference between `==` and `===` in JavaScript?
  - The `===` compares the exact values and `==` is like one level difference.
  - `Null == Undefined` returns `true` but `Null === Undefined` returns `false`
9. Why do front end frameworks exist?
  - To make life easier for Devs!

#### Review  

10. Why do people say "HTTP is stateless"?
  - Because it doesn't automatically store any data about different user/server transactions
  - The information is lost once the transaction ends
11. Describe a RESTful API.
  - Client–server: The client handles the front end the server handles the backend and can both be replaced independently of each other.
  - Stateless: No client data is stored on the server between requests and session state is stored on the client.
  - Cacheable: Clients can cache response (just like browsers caching static elements of a web page) to improve performance.
12. What are some main characteristics of a team following an agile workflow?
  - Highly communicative, regular team checkins
  - Team members taking small "stories" to work on
  - Quick "sprint" work schedules, 2-6 weeks per feature
13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
  - Advantages: 
    - You aren't storing user passwords on your DB. Nothing to hack
    - You get access to the API endpoints of the service that you use for OAuth
      
  - Disadvantages:
    - It is dependent on Users having an account with the OAuth provider
    - You sacrifice control
  
