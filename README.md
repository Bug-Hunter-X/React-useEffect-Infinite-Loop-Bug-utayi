# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook that causes an infinite render loop.  The issue arises from an incorrectly specified dependency array, leading to unintended re-renders.

## Bug Description
The `useEffect` hook in `bug.js` is intended to log the current count. However, the missing dependency array or incorrect dependencies results in the effect running after every render, including the one triggered by the effect itself. This creates a continuous loop of renders, causing performance issues and potentially crashing the application.

## Solution
The solution in `bugSolution.js` correctly specifies the `count` variable in the dependency array.  This ensures that the effect only runs when the `count` value changes, preventing the infinite loop.