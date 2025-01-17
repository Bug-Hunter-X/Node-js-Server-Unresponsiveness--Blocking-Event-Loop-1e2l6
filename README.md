# Node.js Server Unresponsiveness: Blocking Event Loop

This repository demonstrates a common issue in Node.js applications: blocking the event loop with a long-running synchronous operation.  This leads to server unresponsiveness and poor performance.

The `bug.js` file contains the problematic code, while `bugSolution.js` shows the corrected version using asynchronous operations.

## Bug Description

A synchronous loop in the HTTP request handler occupies the event loop, preventing the server from processing other requests. This results in the server becoming unresponsive.

## Solution

The solution involves refactoring the code to use asynchronous operations. This allows other events to be processed while the long-running task executes in the background without blocking the event loop.