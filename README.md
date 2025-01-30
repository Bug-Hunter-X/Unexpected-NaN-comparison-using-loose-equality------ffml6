# JavaScript NaN Loose Equality Bug

This repository demonstrates a common pitfall in JavaScript involving the comparison of NaN (Not a Number) values using the loose equality operator (`==`).

## The Problem

In JavaScript, `NaN` is unique in that it is never equal to itself, even when using loose comparison. This behavior often leads to unexpected results and bugs in programs that handle potentially invalid numerical inputs.

The example file (`bug.js`) showcases this problem.  The `foo` function attempts to check for equality between two values, including potential `NaN` values. However, due to the way loose comparison treats `NaN`, the result is incorrect when both arguments are `NaN`.

## The Solution

The solution file (`bugSolution.js`) demonstrates the proper method for checking for `NaN` values: using the `Number.isNaN()` function.  This method reliably identifies `NaN` and correctly handles the comparison.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` and run the code in a JavaScript environment (browser console, Node.js).
3. Observe the incorrect output.
4. Open `bugSolution.js` and observe the correct handling of NaN using `Number.isNaN()`.

## Key takeaway

Always use `Number.isNaN()` to reliably test for `NaN` instead of relying on loose equality checks.