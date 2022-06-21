# Event-Driven Programming

Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.

Every time you interact with a webpage through its user interface, an event is happening. When you click a button a click event is triggered. When you press a key a keydown event is triggered. These events have associated functions that, when triggered, are executed to make a change to the user interface in some way.


-	Event-Driven Programming makes use of the following concepts:

•	An Event Handler is a callback function that will be called when an event is triggered.

•	A Main Loop listens for event triggers and calls the associated event handler for that event.


## EventEmitter

Node.js natively provides us with a useful module called EventEmitter that allows us to get started incorporating Event-Driven Programming in our project right away. Of course, creating our own version of EventEmitter wouldn’t be much of a challange, and in fact there are several modules published on npm such as EventEmitter2 and EventEmitter3 which promise a faster performance than the native EventEmitter.


```js
const EventEmitter = require('events').EventEmitter;

const chatRoomEvents = new EventEmitter;


function userJoined(username){

  alertAllUsers('User ' + username + ' has joined the chat.');
}

chatRoomEvents.on('userJoined', userJoined);

function login(username){

  chatRoomEvents.emit('userJoined', username);
}
```

## Removing Listeners

There will likely come a time when you want to remove an event listener from an event. This could be for performance reasons (the event is no longer needed) or to avoid memory leaks (if an event listener references an object that is no longer needed, it won’t be able to be garbage-collected. This can lead to a build up of unnecessary objects).

```js
const EventEmitter = require('events').EventEmitter;

const chatRoomEvents = new EventEmitter;


function displayMessage(message){

  document.write(message);
}

function userJoined(username){

  chatRoomEvents.on('message', displayMessage);
}
```

chatRoomEvents.on('userJoined', userJoined);

chatRoomEvents.removeListener('message', displayMessage);

Object Oriented Programming + Event-Driven Programming

The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit. Using this approach, applications are built with many different units that all speak to and interact with each other.


```js
const EventEmitter = require('events').EventEmitter;

const myGatorEvents = new EventEmitter;

class Food {

  constructor(name) {

    this.name = name;

    myGatorEvents.on('gatorEat', this.becomeEaten);

  }

  becomeEaten(){

    return 'I have been eaten.';

  }
}

var bacon = new Food('bacon');

const gator = {

  eat() {

    myGatorEvents.emit('gatorEat');

  }
}
```