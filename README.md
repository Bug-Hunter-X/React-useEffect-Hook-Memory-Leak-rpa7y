# React useEffect Hook Memory Leak

This example demonstrates a common error in React's `useEffect` hook: forgetting to include a return statement for cleanup. This can lead to memory leaks and unexpected behavior.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected version.

## Problem

In the `useEffect` hook, the absence of a return statement prevents the cleanup function from executing when the component unmounts or updates.  This can cause memory leaks if the effect performs actions that need to be cleaned up, such as setting timers or event listeners.