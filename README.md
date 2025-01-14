# Express.js Server Unresponsiveness

This repository demonstrates a common issue in Express.js applications where a long-running synchronous operation in a request handler can block the event loop, making the server unresponsive.

## Bug Description

The `bug.js` file contains an Express.js server with a request handler that simulates a long-running asynchronous operation using `setTimeout`.  However, if this operation were truly synchronous (e.g., a complex database query or file I/O operation), it would block the event loop, preventing other requests from being handled. This can lead to the server appearing unresponsive.

## Solution

The `bugSolution.js` file provides a solution that addresses this by using asynchronous methods appropriately to avoid blocking the event loop.