# React useEffect setInterval Memory Leak

This example demonstrates a common mistake when using `setInterval` inside a React `useEffect` hook: forgetting to include a cleanup function to clear the interval when the component unmounts. This can lead to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a count every second.  However, it fails to clear the interval when the component is unmounted, causing the interval to continue running even after the component is no longer rendered. This will lead to a memory leak.

## Solution

The `bugSolution.js` file provides a corrected version of the component that properly handles the `setInterval` cleanup using the return value of `useEffect`. This ensures that the interval is cleared when the component is unmounted, preventing memory leaks.