# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by a missing dependency in the `useEffect` hook.  The `useEffect` hook is used to perform side effects after a component renders. If a dependency is omitted, the effect runs on every render, potentially leading to an infinite loop. This example illustrates the bug and its solution.

## Bug
The `bug.js` file contains the buggy code.  The `useEffect` hook has an empty dependency array `[]`, causing it to run after every render, regardless of changes in state. This leads to an infinite loop, as each render triggers another effect, causing another render, and so on.

## Solution
The `bugSolution.js` file demonstrates the correct approach.  The `count` variable is added to the dependency array `[count]`. The `useEffect` hook only executes when the `count` state changes, fixing the infinite loop issue.