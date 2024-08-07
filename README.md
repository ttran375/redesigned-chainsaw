# WebSockets

## Agenda 1: WebSocket establishes a handshake between server and client

```sh
yarn add uuid websocket
```

`server/index.js`

```js
const { WebSocketServer } = require("ws");
const http = require("http");

// Spinning the http server and the WebSocket server.
const server = http.createServer();
const wsServer = new WebSocketServer({ server });
const port = 8000;
server.listen(port, () => {
  console.log(`WebSocket server is running on port ${port}`);
});
```
