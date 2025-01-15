# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by incorrectly updating state within the `useEffect` dependency array.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version.

## Bug Description

The `useEffect` hook in `MyComponent` attempts to increment the `count` state within its dependency array. This creates a loop because every time `count` changes, `useEffect` is triggered again, causing `count` to change indefinitely.