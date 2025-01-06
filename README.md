# MongoDB $inc Operator with String Value
This example demonstrates an uncommon error that can occur when using the `$inc` operator in MongoDB update operations.  The `$inc` operator is used to increment a numeric field by a specified value.  However, if a string is provided as the increment value, MongoDB will not throw an error but the result will likely be unexpected.

## Bug
The bug lies in the use of the `$inc` operator with a string value ('1') instead of a numeric value (1).  This leads to the field being updated in an unexpected manner rather than a simple increment.

## Solution
The solution involves ensuring that the value used with `$inc` is a number.  This fixes the update operation and provides the correct result.