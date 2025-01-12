# Unhandled Promise Rejection in Express.js Middleware

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous middleware.  When an asynchronous operation within a route handler throws an error and isn't caught, the Express.js server will crash. This example showcases the problem and provides a solution.

## Bug

The `bug.js` file contains an Express.js application with a route handler that performs an asynchronous operation.  This operation is designed to simulate a failure, throwing an error.  Crucially, the `catch` block is missing which results in the application crashing.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle errors in asynchronous middleware using a `catch` block.  This prevents the application from crashing and allows for graceful error handling.