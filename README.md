# MongoDB $inc Operator Usage Error
This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries.
The `$inc` operator is used to increment or decrement a numeric field in a document.  However, it is crucial to ensure the field exists and is of numeric type before applying `$inc`. Incorrect usage can result in unexpected behavior or errors.

## Bug
The `bug.js` file shows how passing a non-numeric value to `$inc` throws an error. It also shows a situation where applying `$inc` to a non-existent field does not result in an expected increment. 

## Solution
The `bugSolution.js` file demonstrates the correct approach, including validation of the field type and handling of cases where the field doesn't exist by using `$setOnInsert` and `$inc` together to ensure atomicity.
