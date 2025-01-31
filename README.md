# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that occurs when using `setTimeout` within a loop.  The problem arises because the closure created by `setTimeout` doesn't capture the value of `i` at the time of its creation, but instead captures a reference to the variable `i`.  This means that by the time `setTimeout` finally executes, the loop may have already completed, resulting in the same value of `i` (which will be 10) being logged repeatedly.

The `bug.js` file contains the buggy code, and the `bugSolution.js` file demonstrates a corrected version using an immediately invoked function expression (IIFE) to capture the value of `i` at the time `setTimeout` is called.