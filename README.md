# React UseEffect SetInterval Memory Leak
This example demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook: forgetting to clear the interval on unmount.  This leads to a memory leak, as the interval continues to run even after the component is removed from the DOM.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides the corrected version, using `clearInterval` to prevent the memory leak.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Observe the console for any warnings or errors.
5. Note that without the fix, the counter will continue to increment even after the component is unmounted.