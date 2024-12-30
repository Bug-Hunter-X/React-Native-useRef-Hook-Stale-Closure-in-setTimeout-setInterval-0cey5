# React Native useRef Hook Stale Closure in setTimeout/setInterval

This repository demonstrates a common bug in React Native involving the `useRef` hook and its interaction with `setTimeout` or `setInterval`.  When a function is passed to `setTimeout` or `setInterval`, it creates a closure that captures the value of the `ref` at the time of its creation. This can cause issues if the `ref`'s value is updated after the function is created but before it's executed.

The `useRefStaleClosureBug.js` file shows the bug in action, while `useRefStaleClosureSolution.js` provides a solution using a ref callback or updating the value through a state variable.