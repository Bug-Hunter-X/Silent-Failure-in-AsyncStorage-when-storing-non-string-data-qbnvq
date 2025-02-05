# Silent Failure in AsyncStorage when storing non-string data

This repository demonstrates a common issue in React Native development where AsyncStorage silently fails when attempting to store non-string data.  The bug is that AsyncStorage only supports string values and trying to store other data types will lead to unexpected behavior. This example shows how this occurs and provides a solution using JSON.stringify and JSON.parse for proper data serialization and deserialization.

## Bug
The bug is located in `bug.js`. Attempting to store the object directly leads to unpredictable behavior. 

## Solution
The solution in `bugSolution.js` uses `JSON.stringify` to convert the object into a string before storage and `JSON.parse` to convert it back to an object upon retrieval. This ensures compatibility with AsyncStorage.
