# React Native: Handling 'Cannot read properties of undefined (reading 'property')' Errors

This repository demonstrates a common error in React Native applications: 'Cannot read properties of undefined (reading 'property')'.  This error typically occurs when you attempt to access a property of an object that is currently `undefined` or `null`. This is frequently encountered when dealing with asynchronous data fetching or uninitialized component state.

The `bug.js` file showcases code that will produce this error. The `bugSolution.js` file provides the solution.

## Problem

The problem lies in accessing properties of `userData` before the asynchronous `fetchUserData()` function has successfully populated it with data.  If the component renders before the data is available, `userData` remains `null`, leading to the error.

## Solution

The solution is to employ conditional rendering or optional chaining to gracefully handle cases where `userData` might be `null` or `undefined`.

## How to reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npx react-native run-android` (or `npx react-native run-ios`) to run the app.
5. Observe the error in the `bug.js` example.
6. Compare it to the corrected implementation in `bugSolution.js`.