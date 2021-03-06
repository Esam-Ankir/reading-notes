# Socket.IO 

Socket.IO is a JavaScript library for real-time web applications. It enables real-time, bi-directional communication between web clients and servers. It has two parts − a client-side library that runs in the browser, and a server-side library for node.js. Both components have an identical API.

## Real-time Applications

A real-time application (RTA) is an application that functions within a period that the user senses as immediate or current.

Some examples of real-time applications are –

-	Instant messengers − Chat apps like Whatsapp, Facebook Messenger, etc. You need not refresh your app/website to receive new messages.

-	Push Notifications − When someone tags you in a picture on Facebook, you receive a notification instantly.

-	Collaboration Applications − Apps like google docs, which allow multiple people to update same documents simultaneously and apply changes to all people's instances.

-	Online Gaming − Games like Counter Strike, Call of Duty, etc., are also some examples of real-time applications.


## Why Socket.IO?

Writing a real-time application with popular web applications stacks like LAMP (PHP) has traditionally been very hard. It involves polling the server for changes, keeping track of timestamps, and it is a lot slower than it should be.

Sockets have traditionally been the solution around which most real-time systems are architected, providing a bi-directional communication channel between a client and a server. This means that the server can push messages to clients. Whenever an event occurs, the idea is that the server will get it and push it to the concerned connected clients.

Socket.IO is quite popular, it is used by Microsoft Office, Yammer, Zendesk, Trello,. and numerous other organizations to build robust real-time systems. It one of the most powerful JavaScript frameworks on GitHub, and most depended-upon NPM (Node Package Manager) module. Socket.IO also has a huge community, which means finding help is quite easy.

## ExpressJS

We will be using express to build the web server that Socket.IO will work with. Any other node-server-side framework or even node HTTP server can be used. However, ExpressJS makes it easy to define routes and other things. 


## Socket.IO – Environment

To get started with developing using the Socket.IO, you need to have Node and npm (node package manager) installed. If you do not have these, head over to Node setup to install node on your local system

## Socket.IO - Event Handling
Sockets work based on events. There are some reserved events, which can be accessed using the socket object on the server side.
These are –

-	Connect

-	Message

-	Disconnect

-	Reconnect

-	Ping

-	Join 

-	Leave.


The client-side socket object also provides us with some reserved events, which are –

-	Connect

-	Connect_error

-	Connect_timeout

-	Reconnect, etc.

