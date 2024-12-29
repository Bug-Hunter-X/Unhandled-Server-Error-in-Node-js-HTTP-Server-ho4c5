# Unhandled Server Error in Node.js HTTP Server

This repository demonstrates a common error in Node.js HTTP server development: failure to handle potential errors during server creation and listening.  The `bug.js` file contains the erroneous code, while `bugSolution.js` provides a corrected version with robust error handling.

## Bug Description

The original code creates a simple HTTP server but omits error handling.  If port 8080 is already in use or there's another issue starting the server, the application crashes without providing informative error messages.

## Solution

The improved code in `bugSolution.js` incorporates error handling using the `'error'` event listener of the HTTP server.  This listener catches potential errors and logs them to the console, providing crucial debugging information.  The server also gracefully handles `'listening'` event for confirming server status. 

## How to run

1. Clone the repository: `git clone <repository_url>`
2. Navigate to the repository directory.
3. Run the buggy code (bug.js) using `node bug.js` and observe the result when port 8080 is already in use. 
4. Run the corrected code (bugSolution.js) using `node bugSolution.js` and observe the improved error handling. 