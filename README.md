# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. Specifically, the example shows a route that fetches a user by ID.  If the ID is not a valid number, the code will throw an error.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version with proper error handling.

## Bug

The main issue lies in the lack of input validation. The code directly attempts to parse the `userId` as an integer using `parseInt()` without checking if it's actually a number. If a non-numeric string is passed as the ID, `parseInt()` will return `NaN`, leading to a potential crash or unexpected behavior when trying to find a user with that ID.

## Solution

The corrected code in `bugSolution.js` adds input validation to check if the `userId` is a number before proceeding. If it's not a number, an appropriate error response is sent back to the client.  This prevents unexpected errors and ensures the application remains robust.

This example highlights the importance of thorough error handling and input validation in Express.js applications to prevent crashes and enhance security.