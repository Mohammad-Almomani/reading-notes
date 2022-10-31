# Reading Socket

## The OSI Model

1. What the OSI model is

   The Open Systems Interconnection (OSI) model describes seven layers that computer systems use to communicate over a network. It was the first standard model for network communications, adopted by all major computer and telecommunication companies in the early 1980s

2. What are the 7 layers of OSI model

   - Layer 1: Physical Layer
   - Layer 2: Data Link Layer
   - Layer 3: Network Layer
   - Layer 4: Transport Layer
   - Layer 5: Session Layer
   - Layer 6: Presentation Layer
   - Layer 7: Application Layer

## Socket.io

1.  What is a socket?

    A socket is an endpoint of communication, and it is the place where data is sent and received. It is a combination of an IP address and a port number. The IP address identifies the computer, and the port number identifies the specific process or application on the computer.

2.  What is Socket.io?

    Socket.IO is a library that enables real-time, bidirectional and event-based communication between the browser and the server. It consists of:

    - a Node.js server: Source | API
    - a Javascript client library for the browser (which can be also run from Node.js): Source | API

3.  Example on Socket.io Server API?

```js
    io.on('connection', (socket) => { ... });
    socket.emit('request', /* … */); // emit an event to the socket
    io.emit('broadcast', /* … */); // emit an event to all connected sockets
    socket.on('reply', () => { /* … */ }); // listen to the event
```

4. Example on Socket.io Client API?

```js
io.connect();
socket.emit("news", { hello: "world" });
socket.on("my other event", (data) => {
  console.log(data);
});
```
