# React useEffect Hook - Missing Dependency
This example demonstrates a common error in React's `useEffect` hook: forgetting to include dependencies in the dependency array.  This can lead to unexpected behavior, most notably, infinite render loops.

## Problem
The `useEffect` hook is intended to perform side effects after a component renders.  When dependencies are omitted (or incorrectly specified), the effect runs on every render. In this case, the log statement executes repeatedly, which isn't inherently problematic but could lead to performance issues.

More critical issues arise when you use functions like `fetch` or update a state based on the current state inside `useEffect` without specifying the correct dependencies in the array.