# ES6 Classes and  Express Routing

## ES6 Classes

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.
difference between function declarations and class declarations:
functions can be called in code that appears before they are defined, classes must be defined before they can be constructed.

class syntax has two components: class expressions and class declarations:
class declarations: class class_name{}
class expressions:Unnamed: let class_name=class{}, Or named:  let class_name=class exp_name

### Prototype methods

class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

  // Getter
  get area() {
    return this.calcArea();
  }

  // Method
  calcArea() {
    return this.height * this.width;
  }
}

### Generator methods
class Polygon {
  constructor(...sides) {
    this.sides = sides;
  }

  // Method
  *getSides() {
    for(const side of this.sides){
      yield side;
    }}}

### Static methods
class Animal {
  speak() {
    return this;
  }
  static eat() {
    return this;
  }
}

let obj = new Animal();
obj.speak(); // the Animal object
let speak = obj.speak;
speak(); // undefined

Animal.eat() // class Animal
let eat = Animal.eat;
eat(); // undefined

### Field declarations
Public field declarations
Private field declarations using #


## Routing

Routing refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method (GET, POST, and so on).
Each route can have one or more handler functions, which are executed when the route is matched.

### Route structure:

**App.METHOD(PATH, HANDLER)**

Where:
•	app is an instance of express.
•	METHOD is an HTTP request method, in lowercase.
•	PATH is a path on the server.
•	HANDLER is the function executed when the route is matched.


**app.get()** to handle GET requests 
**app.post()** to handle POST requests.
**app.all()** to handle all HTTP methods 
**app.use()** to specify middleware as the callback function 
**app.route()** to create chainable route handlers for a route path
**express.Router()** to create modular, mountable route handlers
**res.download()** to Prompt a file to be downloaded.
**res.end()** to End the response process.
**res.json()** to Send a JSON response.
**res.jsonp()** to Send a JSON response with JSONP support.
**res.redirect()** to Redirect a request.
**res.render()** to Render a view template.
**res.send()** to Send a response of various types.
**res.sendFile()** to Send a file as an octet stream.
**res.sendStatus()** to Set the response status code and send its string representation as the response body.

### To Use the New Router in ExpressJS 4.0, we can:
•	Use express.Router() multiple times to define groups of routes
•	Apply the express.Router() to a section of our site using app.use()
•	Use route middleware to process requests
•	Use route middleware to validate parameters using .param()
•	Use app.route() as a shortcut to the Router to define multiple requests on a route







