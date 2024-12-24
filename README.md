# Node.js Server Hang: Synchronous Operation

This repository demonstrates a common Node.js issue: a server hanging due to a long-running synchronous operation within the request handler.  The `bug.js` file contains the problematic code, while `bugSolution.js` offers a solution using asynchronous operations.

**Problem:** The synchronous `while` loop in `bug.js` blocks the event loop, preventing the server from responding to further requests.  This can lead to unresponsive servers and poor performance.

**Solution:** The `bugSolution.js` file refactors the code to use asynchronous operations. This allows the event loop to continue processing other requests while the long-running task executes.