# Message Queues

## Introduction
Writing a chat application with popular web application stacks like LAMP (PHP) has normally been very hard. It involves polling the server for changes, keeping track of timestamps, and it’s a lot slower than it should be.

Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server.

This means that the server can push messages to clients. Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients.

## Rooms
A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients.

### Joining and leaving

You can call join to subscribe the socket to a given channel:
```js
io.on("connection", async (socket) => {

  const projects = await fetchProjects(socket);

  projects.forEach(project => socket.join("project:" + project.id));

  // and then later

  io.to("project:4321").emit("project updated");

});
```

### Disconnection
Upon disconnection, sockets leave all the channels they were part of automatically, and no special teardown is needed on your part.

You can fetch the rooms the Socket was in by listening to the disconnecting event:
```js
io.on("connection", socket => {

  socket.on("disconnecting", () => {

    console.log(socket.rooms); // the Set contains at least the socket ID

  });


  socket.on("disconnect", () => {

    // socket.rooms.size === 0

  });

});
```

With multiple Socket.IO servers

```js
// main namespace

const rooms = io.of("/").adapter.rooms;

const sids = io.of("/").adapter.sids;


// custom namespace

const rooms = io.of("/my-namespace").adapter.rooms;

const sids = io.of("/my-namespace").adapter.sids;
```

## Namespaces
A Namespace is a communication channel that allows you to split the logic of your application over a single shared connection (also called "multiplexing").

Each namespace has its own:
•	event handlers

•	rooms

•	middlewares

```js
io.on("connection", (socket) => {});

io.use((socket, next) => { next() });

io.emit("hello");

// are actually equivalent to

io.of("/").on("connection", (socket) => {});

io.of("/").use((socket, next) => { next() });

io.of("/").emit("hello");
```


[check out Emit cheatsheet](https://socket.io/docs/v4/emit-cheatsheet/)
