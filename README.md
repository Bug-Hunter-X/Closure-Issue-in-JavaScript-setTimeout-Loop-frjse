# Closure Issue in JavaScript setTimeout Loop
This repository demonstrates a common closure-related bug in JavaScript when using `setTimeout` within a loop.  The problem arises because the `setTimeout` callback functions don't capture the value of `i` at the time they're created; instead, they capture a reference to `i`.  This leads to all callbacks logging the final value of `i` (10), instead of the expected 0-9.

## How to Reproduce
1. Clone the repository.
2. Open `bug.js` and run it in a JavaScript environment (e.g., a browser's console or Node.js).
3. Observe that the console logs '10' ten times instead of 0 through 9.

## Solution
The solution involves using an immediately invoked function expression (IIFE) or `let` (which has block scope) to create a new scope for each iteration of the loop, thereby capturing the correct value of `i`.

## License
MIT