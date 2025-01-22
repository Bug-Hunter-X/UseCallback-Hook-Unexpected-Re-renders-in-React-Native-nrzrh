# useCallback Hook Unexpected Re-renders in React Native

This repository demonstrates a common but subtle error in React Native when using the `useCallback` hook.  The error arises when a function passed to `useCallback` directly uses a state variable within its body, even if an empty dependency array `[]` is provided to `useCallback`. This results in the function being recreated unnecessarily on every state change, leading to unexpected behavior.

The `bug.js` file shows the problematic code.  The solution, in `bugSolution.js`, demonstrates the correct way to handle this scenario.