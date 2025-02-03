# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The issue arises from omitting the dependency array in `useEffect`, leading to an infinite loop and application crash.

## Bug Description

The `bug.js` file contains a `MyComponent` that uses the `useEffect` hook to log the current `count` to the console.  Because the dependency array is missing, the effect runs after every render, causing a continuous loop of updates and log messages. This eventually overwhelms the browser and crashes the application.

## Solution

The `bugSolution.js` file provides a corrected version. The dependency array `[count]` is added to `useEffect`. Now, the effect only runs when the `count` value changes, preventing the infinite loop. 

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Observe the console and the erratic behavior of the counter in `bug.js`.
5. Compare and contrast with the stable counter in `bugSolution.js`.