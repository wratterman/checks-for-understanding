## Week Four - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's your favorite project management tool?
  - Personally, I like Waffle.io for the simplicity. But I see why Pivitol is used on by companies. It is a good one stop shop for everyone to be aware of what is being worked on. 
2. Why do we create staging environments?
  - So that we can create environments as close to different production environments as possible before deploying.
3. What are the characteristics of a good README (in your opinion)?
  - References to contributers
  - Setup Instructions
    - Links to external keys/packages/etc. needed
  - How to Run/Use
  - Features you wish to highlight
  - Instructions on contribution (if offered)
4. What's one main improvement you're going to make to your code regarding accessibility issues?
  - Being aware of color-blindness and dyslexia when choosing colors/fonts for CSS/SASS
  - Utilization of buttons instead of links for people who need to use `tab` instead of a mouse
5. What are some basic security concerns to be aware of when building applications?
  - If storing passwords, salt
  - Don't publish production keys, tokens, etc.
  - Make sure ORM protects against SQL injection (utilize ORM instead of raw SQL if possible), or sanitize information coming from params manually before passing to SQL query,
6. Why is continuous integration helpful/important?
  - It's an additional level of testing that we can introduce to our program including running with different versions of different languages to help indentify bugs. 
7. What are some continuous integration tools?
  - TravisCI, Jenkins, CircleCI

#### Review  

8. What are some characteristics of "good" git workflow?
  - Checking out branches based on feature/task/bug/etc and creating PRs for review when complete
  - Not merging your own PR
  - Multiple comments attached to code snippets when reviewing PRs & issues
  - `@`ing other contributers to alert them when they are ready for review
  - Summary when submitting something for review, breakdown of key parts, requests for help specifically
9. What are the four fundamental concepts of object oriented programming?
  - Abstraction
  - Encapsilation
  - Inheritance
  - Polymorphism
10. What's a module in Ruby and what's the difference between a class and a module?
  - A class can hold state while a module cannot. A module can contain methods that can be included into other classes. Instances of that class will be able to call those methods. For instance...
```ruby
module ExampleModule
  def speak
    return "Hello"
  end
end

class Example
  include ExampleModule

  def say_name
    return "I am Example!"
  end
end

class Carl
  include ExampleModule

  def say_name
    return "I am Carl"
  end
end

example = Example.new
carl    = Carl.new

example.speak
=> "Hello"
carl.speak
=> "Hello"
example.say_name
=> "I am Example!"
carl.say_name
=> "I am Carl!"
```
