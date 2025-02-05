# Node.js Server Hanging on Long Requests

This repository demonstrates a common issue in Node.js where long-running requests can cause the server to become unresponsive.  The problem stems from blocking the event loop, preventing it from handling other requests or events.

## Problem

The `server.js` file contains a simple HTTP server that simulates a long-running task (a 5-second wait). During this wait, the server is unable to handle any new requests, effectively hanging.

## Solution

The `server-solution.js` file demonstrates a solution using asynchronous operations.  Instead of blocking the event loop, it uses `setTimeout` to handle the long-running task asynchronously.  This allows the server to remain responsive to other requests while the task is executing.