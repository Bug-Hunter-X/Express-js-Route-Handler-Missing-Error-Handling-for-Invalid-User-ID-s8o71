# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the example shows a route that fetches a user by ID.  If the ID is not a valid number, the application will likely crash or behave unexpectedly.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version with comprehensive error handling.

## Bug

The primary issue is the absence of input validation. The code attempts to parse the `userId` as an integer without checking if it's a valid number. If the `userId` is not a number (e.g., a string), `parseInt(userId)` will return `NaN`, leading to errors.

## Solution

The solution involves adding input validation to check if the `userId` is a number before attempting to use it. If it's not a number, the route should return an appropriate error response.