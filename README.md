# Express.js: Empty JSON Request Body Handling

This repository demonstrates a common issue in Express.js applications where empty JSON request bodies are not handled correctly. The application fails to parse an empty JSON body and logs an empty object to the console instead of providing informative error handling.

## Bug Description
The provided Express.js server is designed to receive JSON data via a POST request to `/data`. However, when an empty JSON request body is sent, the server does not throw an error or handle it gracefully.  Instead, `req.body` is an empty object, which can lead to unexpected behavior and potential vulnerabilities.

## Solution
The solution involves adding middleware to check for empty request bodies and handle them appropriately. This might involve returning an error response or logging a more descriptive message.

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install Express.js.
3. Run `node bug.js` to start the server.
4. Send a POST request to `http://localhost:3000/data` with an empty JSON body.
5. Observe the empty object logged to the console.
6. Run `node bugSolution.js` to see the improved error handling.
