# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue in Express.js applications where parsing the JSON request body fails when the body is empty or contains invalid JSON.  The issue arises from the lack of proper error handling when `express.json()` encounters malformed data.

## Bug

The `bug.js` file contains an Express.js server that attempts to parse JSON from POST requests to the `/data` endpoint. If the request body is empty or contains invalid JSON, the server will throw an error and crash.

## Solution

The `bugSolution.js` file provides a solution that adds error handling to gracefully manage these situations. It uses a try-catch block to handle parsing errors, returning an appropriate error response to the client instead of crashing the server.