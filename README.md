# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can make the server unresponsive.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

**Problem:** The original code blocks the event loop for 5 seconds, preventing it from processing other requests. This leads to an unresponsive server.

**Solution:** The solution uses asynchronous operations to avoid blocking the event loop, ensuring the server remains responsive even during long-running tasks.