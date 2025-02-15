# Unhandled JSON Property Access in Dart

This repository demonstrates a common error in Dart when handling JSON responses: attempting to access a property of a JSON object without checking for its existence.  This can lead to runtime exceptions if the expected property is missing.

The `bug.dart` file contains the buggy code. The `bugSolution.dart` file provides a corrected version that handles missing properties gracefully.

## Bug Description
The code fetches JSON data from an API. It then iterates through the JSON array and attempts to access the `name` property of each item.  If any item lacks a `name` property, a runtime error occurs.

## Solution
The solution involves checking for the existence of the `name` property before accessing it.  This can be done using the `containsKey()` method or optional chaining.