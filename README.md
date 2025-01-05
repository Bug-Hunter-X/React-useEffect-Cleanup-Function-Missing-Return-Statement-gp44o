# React useEffect Cleanup Function Missing Return Statement

This repository demonstrates a common React bug: a missing `return` statement in a `useEffect` cleanup function. This can lead to memory leaks and unexpected behavior.

## Bug Description

The `useEffect` hook in `bug.js` adds an event listener. However, it lacks a return statement to remove the event listener when the component unmounts or updates.  This results in the event listener persisting, potentially causing memory leaks and unexpected behavior.

## Solution

The solution (`bugSolution.js`) adds a return statement to the `useEffect` function that removes the event listener. This ensures proper cleanup and avoids the memory leak.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output to check for memory leaks (you'll need to use browser developer tools).