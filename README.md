# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js servers: unresponsiveness caused by long-running synchronous operations within the request handler.  The `server.js` file contains a simple HTTP server that performs a computationally intensive task (a large loop) before sending a response. This blocks the event loop, preventing the server from handling other requests and leading to unresponsiveness.

The solution (`serverSolution.js`) demonstrates how to address this using asynchronous operations or by offloading the task to a worker thread.