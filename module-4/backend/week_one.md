## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
  - I liked event targeting and using that to access the desired attributes and use that in a variety of ways.
2. What are some tools to help debug JavaScript code?
  - Browser Dev Tools, debugger, pryjs, console.log(), etc.
3. What are some tools you need in order to unit test your JavaScript?
  - Mocha, Chai
4. What is the syntax for invoking a function?
```javascript
function exampleFunction() {
  // ... do a thing
};

exampleFunction(); // <--- invoking
```
5. What's `this` in JavaScript?
  - Similar to `self` in Ruby. Kind of a snapshot of whatever is being interacted with, often (if not always) with the ability to invoke functions and attributes that belong to that object.
6. What is Webpack and why is it useful?
  - Webpack compiles your JS and CSS into one file for you, so you can abstract your code into seperate files then import them in one place.
7. When/why do you want to use event delegation?
  - To identify what is being interacted with/their parent element(s). You would use it in a situation where you need some information stored as an attribute to include in your code.
8. What's `npm` and what do we use it for?
  - Node Package Manager. We use it to manage our node packages. We install libraries using npm, we start our server using npm, it acts as a bundler. It manages our packages.

#### Review  
9. What's the MVC design pattern? Describe each part of MVC.
  `M`odel `V`iew `C`ontroller
   - Client (user cpu) --(http)-> Router inside the Server
   - Router determines which controller and action the client is requesting ---> Controller
   - Controller determines which database models are needed for the page (if any) ----> Model
   - Model submits appropriate query to databse ----> Database (through the ORM in the case of ActiveRecord)
   - Database returns the models, ORM converts to objects ---> Models 
   - Model Returns the correct model object(s) to the original controller ----> Controller
   - Controller, now with the data sends the objects to the views to be displayed ---> Views
   - Objects are now displayed as desired and the final page is sent back to the client ---> Client (user cpu)  
10. What are a few ways to optimize a Rails application?
  - Caching, background workers/Message Queues, minimizing database queries, etc.
11. What's a background worker? When would we want to use a background worker?
  - A background worker executes code outside of the normal flow of the primary code. It is used to optimize an app by avoiding situations where a specific task takes a prolonged period of time to evaluate. By separating that functionality, the rest of the app can execute. The appropriate response will be sent once the background worker can execute it properly. ex. Credit Card purchase validation. 
