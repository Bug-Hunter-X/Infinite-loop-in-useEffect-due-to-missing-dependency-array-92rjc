# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by a missing dependency array.  The `useEffect` hook, when used without a dependency array or with an incomplete one, will re-run after every render, leading to performance issues and potentially crashes.

## Bug Description

The `bug.js` file contains a `MyComponent` that uses the `useEffect` hook to log the current count to the console. However, the dependency array `[count]` is missing, meaning the effect runs after every render, leading to an infinite loop because `setCount` is called inside the `onClick` handler.