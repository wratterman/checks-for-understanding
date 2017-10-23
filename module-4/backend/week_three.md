## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?
  - Node is a javascript run time environment which allows for code to be run in a server enivronment. 
2. What is Express? What is Express similar to in the Ruby world?
  - Express is a backend framework for building web apps
  - Express is similar to Sinatra
3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.
  - In `server.js`
```javascript
const express = require('express')
const app = express()
const bodyParser = require('body-parser')

app.use(bodyParser.json())
app.use(bodyParser.urlencoded({ extended: true }))

app.set('port', process.env.PORT || 3000)

app.get('/api-url', function(req, res) {
  // do a thing to get all models
  // display as json
})

app.get('/api-url/:id', function(req, res) {
  // do a thing to get a specific model
  // display as json
})
app.post('/api-url', function(req, res) {
  // do a thing to create a new model
  // display as json
})
```
  - or refactored...
  - in `server.js`
```javascript
const express = require('express')
const app = express()
const bodyParser = require('body-parser')
const ExamplesController = require(./lib/controllers/examples) 

app.use(bodyParser.json())
app.use(bodyParser.urlencoded({ extended: true }))

app.set('port', process.env.PORT || 3000)

app.get('/api-url', ExamplesController.index)

app.get('/api-url/:id', ExamplesController.show)

app.post('/api-url', ExamplesController.create)
```
  - And in `lib/controllers/example.js`
```javascript
const Example = require('../models/example') // For SQL queries

const index = (req, res) => {
  // do a thing to get a all models
  // display as json
}

const show = (req, res) => {
  // do a thing to get a specific model
  // display as json
}

const create = (req, res) => {
  // do a thing to create a new model
  // display as json
}

module.exports = {
  index, 
  show,
  create
}
```
4. What do we use Knex for?
  - We use Knex to make queries to our DB and and return objects that can be accessed/interacted with elsewhere in the code.
  - It's our ORM
5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?
  - See #3
6. How do you execute raw SQL in node?
```javascript
const environment = process.env.NODE_ENV || 'development'
const configuration = require('./knexfile')[environment]
const database = require('knex')(configuration)

return database.raw('SELECT * FROM examples;')
.then((data) => {
  // Do a thing with the returned promise. 
  // data.rows = array of database model objects
})
```
7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
  - Advantages: 
    - Connecting by API allows for a large variety of languages to be used for both frontend and backend languages easily
    - More abrstraction by responsibility, frontend vs backend
  
  - Disadvantages: 
    - Host two seperate apps on two servers

#### Review  

8. Describe DNS.
  - Domain Name Servers. This allows for websites to be looked up by the IP address associated with that url
9. What does writing clean code mean to you?
  - Code that is flexible and can be reused.
    - Avoiding 'hard-coded' methods
  - Single responsibility of methods and classes
  - Abstracted by responsibilities
10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?
  - Brand: Contains Hotels
  - Hotels: Contains Floors, Rooms, Restaurant, Event Space, Staff, Outdoor
  - Floors: Contains Rooms, Contructive Materials, FF&E, etc.
  - Rooms: Can be ADA compliant or non-ADA compliant, contain FF&E, constructive materials, etc.
  - Constructive Materials: Foundation, Walling, Plumbing, Lighting, etc
  - FF&E: Furniture, Fixtures & Equiptment. Sofas, Beds, Nightstands, Artwork, etc.
  - ADA: Different required bed height, drapery mechanisms, bathroom equiptment, accessibility to emergency exits, etc. 
