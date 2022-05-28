# **Introduction to Express** 

## Node.js:
 is an open-source, cross-platform runtime environment that allows developers to create all kinds of server-side tools and applications in JavaScript.

### Node benefits:
•	Great performance
•	Code is written in "plain old JavaScript" 
•	JavaScript is a relatively new programming language and many other new and popular languages compile/convert into JavaScript so you can also use TypeScript, CoffeeScript, ClojureScript, Scala, LiveScript, etc.
•	The node package manager (NPM) provides access to hundreds of thousands of reusable packages.
•	It is available on Microsoft Windows, macOS, Linux, Solaris, FreeBSD, OpenBSD, WebOS, and NonStop OS. 
•	It has a very active third-party ecosystem and developer community

### Module in Node.js:
A set of functions you want to include in your application.

## Frameworks:
A framework is a collection of various libraries and tools that are required in the development process of a software application. It acts as a base on which different software applications can be developed. A node framework is a workspace platform that supports the use of Node.js and which allows developers to use JavaScript for developing front end as well as the back end of an application. Node frameworks are a wide collection of frameworks built on Node and that extend its properties and functionalities further.

### Benefits of Node Framework 
•	Productivity
•	Scalability
•	Speed
•	Same Languages for Front-end and Back-end
•	Maintaining Code standards across a team


## Express:
Express is the most popular Node web framework used to:
•	Write handlers for requests with different HTTP verbs at different URL paths (routes).
•	Integrate with "view" rendering engines in order to generate responses by inserting data into templates.
•	Set common web application settings like the port to use for connecting, and the location of templates that are used for rendering the response.
•	Add additional request processing "middleware" at any point within the request handling pipeline.
Express provides methods to specify what function is called for a particular HTTP verb (GET, POST, SET, etc.) and URL pattern ("Route"), and methods to specify what template ("view") engine is used, where template files are located, and what template to use to render a response. You can use Express middleware to add support for cookies, sessions, and users, getting POST/GET parameters, etc. You can use any database mechanism supported by Node (Express does not define any database-related behavior).

## The Middleware function:

 It defines actions to be done before the webpage can be viewed and other functions can be called.
Link for more about Middleware https://expressjs.com/en/resources/middleware.html

## Some express important codes:

### Settings

app.set('x', 'yyy')

app.get('x') //=> 'yyy'

app.enable('trust proxy')

app.disable('trust proxy')

app.enabled('trust proxy') //=> true

### Env

app.get('env')

### Config

app.configure('production', function() {

  app.set...

})

### Wares

app.use(express.static(__dirname + '/public'))

app.use(express.logger())

### Helpers

app.locals({

  title: "MyApp",

})

### Request

// GET  /user/tj

req.path         //=> "/user/tj"

req.url          //=> "/user/tj"

req.xhr          //=> true|false

req.method       //=> "GET"

req.params

req.params.name  //=> "tj"

req.params[0]

// GET /search?q=tobi+ferret

req.query.q // => "tobi ferret"

req.cookies

req.accepted

// [ { value: 'application/json', quality: 1, type: 'application', subtype: 'json' },

//   { value: 'text/html', quality: 0.5, type: 'text',subtype: 'html' } ]

req.is('html')

req.is('text/html')

req.headers

req.headers['host']

req.headers['user-agent']

req.headers['accept-encoding']

req.headers['accept-language']

### Response

res.redirect('/')

res.redirect(301, '/')

res.set('Content-Type', 'text/html')

res.send('hi')

res.send(200, 'hi')

res.json({ a: 2 })


## npm:
npm is the world's largest software registry. Open source used to share and borrow packages, and manage private development.
### npm Uses:
•	Adapt packages of code for your apps, or incorporate packages as they are.
•	Download standalone tools you can use right away.
•	Run packages without downloading using npx.
•	Share code with any npm user, anywhere.
•	Restrict code to specific developers.
•	Create organizations to coordinate package maintenance, coding, and developers.
•	Form virtual teams by using organizations.
•	Manage multiple versions of code and code dependencies.
•	Update applications easily when underlying code is updated.
•	Discover multiple ways to solve the same puzzle.
•	Find other developers who are working on similar problems and projects.

## TDD:
. “Test-driven development” refers to a style of programming in which three activities are tightly interwoven: coding, testing (in the form of writing unit tests) and design (in the form of refactoring).
It can be succinctly described by the following set of rules:
•	write a “single” unit test describing an aspect of the program
•	run the test, which should fail because the program lacks that feature
•	write “just enough” code, the simplest possible, to make the test pass
•	“refactor” the code until it conforms to the simplicity criteria
•	repeat, “accumulating” unit tests over time


## HTTP Status Codes:

### 1xx Informational
100 Continue
101 Switching Protocols
102 Processing (WebDAV)

### 2xx Success
 200 OK
 201 Created
202 Accepted
203 Non-Authoritative Information
 204 No Content
205 Reset Content
206 Partial Content
207 Multi-Status (WebDAV)
208 Already Reported (WebDAV)
226 IM Used
 
### 3xx Redirection
300 Multiple Choices
301 Moved Permanently
302 Found
303 See Other
 304 Not Modified
305 Use Proxy
306 (Unused)
307 Temporary Redirect
308 Permanent Redirect (experimental)

### 4xx Client Error
 400 Bad Request
 401 Unauthorized
402 Payment Required
 403 Forbidden
 404 Not Found
405 Method Not Allowed
406 Not Acceptable
407 Proxy Authentication Required
408 Request Timeout
 409 Conflict
410 Gone
411 Length Required
412 Precondition Failed
413 Request Entity Too Large
414 Request-URI Too Long
415 Unsupported Media Type
416 Requested Range Not Satisfiable
417 Expectation Failed
418 I'm a teapot (RFC 2324)
420 Enhance Your Calm (Twitter)
422 Unprocessable Entity (WebDAV)
423 Locked (WebDAV)
424 Failed Dependency (WebDAV)
425 Reserved for WebDAV
426 Upgrade Required
428 Precondition Required
429 Too Many Requests
431 Request Header Fields Too Large
444 No Response (Nginx)
449 Retry With (Microsoft)
450 Blocked by Windows Parental Controls (Microsoft)
451 Unavailable For Legal Reasons
499 Client Closed Request (Nginx)
 
### 5xx Server Error
 500 Internal Server Error
501 Not Implemented
502 Bad Gateway
503 Service Unavailable
504 Gateway Timeout
505 HTTP Version Not Supported
506 Variant Also Negotiates (Experimental)
507 Insufficient Storage (WebDAV)
508 Loop Detected (WebDAV)
509 Bandwidth Limit Exceeded (Apache)
510 Not Extended
511 Network Authentication Required
598 Network read timeout error
599 Network connect timeout error
 



## Continuous integration, or CI:
 is a workflow strategy that helps ensure everyone's changes will integrate with the current version of the project. This lets you catch bugs, reduce merge conflicts, and have confidence your software is working. While the details may vary depending on your development environment, most CI systems feature the same basic tools and processes. In most scenarios, a team will practice CI in conjunction with automated testing using a dedicated server or CI service. Whenever a developer adds new work to a branch, the server will automatically build and test the code to determine whether it works and can be integrated with the code on the main development branch. The CI server will produce output containing the results of the build and an indication of whether or not the branch passes all the requirements for integration into the main development branch. By exposing build and test information for every commit on every branch, CI paves the way for what's known as continuous delivery, or CD, as well as a related process called continuous deployment.


The difference between continuous delivery and continuous deployment:
Continuous delivery:
 is the practice of developing software in such a way that you could release it at any time. When coupled with CI, continuous delivery lets you develop features with modular code in more manageable increments.

 ## Continuous deployment :
is an extension of continuous delivery. It's a process that allows you to actually deploy newly developed features into production with confidence, and experience little, if any, downtime.Continuous deployment works in a similar way. You can often configure your CI server to deploy branches as part of its processes. In a simple setup, anytime the master branch receives a new commit, the CI provider grabs a current copy of the project, and deploys the master branch to production. The setup for this type of deployment will vary depending on your provider. If your project requires more flexibility, GitHub also exposes a Deployments API that lets you create custom deployments from branches, tags, or commits. You can use the Deployments API in conjunction with webhooks to automatically notify third-party systems, which can then retrieve a copy of the code from GitHub and deploy the version you request to the environment you specify.

## Continuous integration :
is a workflow strategy you can lean on to help you ensure new code will integrate into the current version of the software. Continuous delivery is developing software that could be released at any time. GitHub puts your code at the center of your development ecosystem by serving as a clearinghouse that not only keeps track of changes, but also communicates with other systems about those changes using webhooks and APIs.





