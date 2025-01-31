# React useEffect Hook Missing Return Statement

This repository demonstrates a common error in React applications: forgetting to include a return statement within a `useEffect` hook.  This can lead to memory leaks and unexpected behavior, particularly when dealing with cleanup functions or subscriptions.

## The Bug
The `bug.js` file contains a `useEffect` hook that's missing a `return` statement. This means that any cleanup functions (e.g., canceling subscriptions, clearing timers) are not executed when the component unmounts.  This may result in memory leaks if not handled carefully.

## The Solution
The `bugSolution.js` file provides the correct implementation of the `useEffect` hook.  It includes a return statement that handles the cleanup properly.  This ensures that resources are released when the component is no longer needed.

## How to reproduce the bug:
1. Clone this repo.
2. Run `npm install` to install dependencies
3. Run `npm start` to start the application
4. Notice that the console logs "Count changed" many times, and even after unmounting the component, it may persist.

## How to fix:
Refer to the solution file to observe the correct method of using a return statement in a useEffect hook to handle cleanup functions.
