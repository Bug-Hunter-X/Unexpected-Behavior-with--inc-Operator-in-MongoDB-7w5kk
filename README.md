# Unexpected Behavior with $inc Operator in MongoDB

This repository demonstrates an uncommon error that can occur when using the `$inc` operator in MongoDB. The error arises when attempting to decrement a field that either does not exist or is not a number. This can lead to unexpected behavior or silent failures.

## The Bug
The provided `bug.js` file contains code that attempts to decrement a counter using `$inc` with a negative value. If the `sequence_value` field does not exist or is not a number, the operation may fail without providing an informative error message.

## The Solution
The `bugSolution.js` file shows a more robust way to handle this situation. It first checks for the existence of the `sequence_value` field and ensures it's a number before using the `$inc` operator.