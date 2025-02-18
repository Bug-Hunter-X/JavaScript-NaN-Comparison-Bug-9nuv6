# JavaScript NaN Comparison Bug

This repository demonstrates a common, yet subtle, bug in JavaScript related to comparing NaN (Not a Number) values using the strict equality operator (===).

## The Problem

In JavaScript, NaN (Not a Number) is a special numeric value that represents the result of an invalid numeric operation (e.g., 0/0).  A peculiar characteristic of NaN is that it is *not equal* to itself. This means:

```javascript
NaN === NaN; // false
```

This behavior can lead to unexpected results in conditional statements.  The provided code illustrates a function that incorrectly returns `false` when comparing two NaN values.

## Solution

To reliably compare NaN values, it's recommended to use the `Number.isNaN()` function instead of direct comparison using `===`. This function specifically checks if a value is NaN.

## How to Run

1. Clone the repository.
2. Navigate to the project directory in the terminal.
3. Open `bug.js` to see the buggy code.
4. Open `bugSolution.js` to see the corrected code.
5. Run both files using Node.js (or your preferred JavaScript runtime):
   ```bash
   node bug.js
   node bugSolution.js
   ```