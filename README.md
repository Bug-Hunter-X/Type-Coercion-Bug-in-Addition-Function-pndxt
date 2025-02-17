# Type Coercion Bug in JavaScript Addition Function

This repository demonstrates a subtle bug in a JavaScript function that performs addition. The bug arises from the function's handling of null values and its implicit type coercion.

## Bug Description

The `foo` function is intended to add two numbers. However, it incorrectly returns `null` if either of the inputs is `0`, treating `0` as equivalent to `null`. This is because the strict equality operator (`===`) is used and `0` is not strictly equal to `null`.

## Solution

The solution involves explicit type checking using `typeof` operator instead of direct comparison with `null`.  This approach accurately differentiates between numbers (including 0) and `null` values, thereby avoiding the incorrect `null` return.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` to see the problematic code.
3. Open `bugSolution.js` to see the fixed code.
4. Run the code using a Node.js environment (or a browser console). Observe the different outputs of the original and fixed versions when either 'a' or 'b' is 0.
