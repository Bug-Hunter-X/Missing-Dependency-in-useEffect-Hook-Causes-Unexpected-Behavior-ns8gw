# Missing Dependency in useEffect Hook

This repository demonstrates a common error in React applications: forgetting to include necessary variables in the dependency array of the `useEffect` hook.  This can lead to unexpected re-renders, performance issues, and even infinite loops.

The `bug.js` file showcases the incorrect implementation. The `useEffect` hook attempts to log the current `count` but omits `count` from its dependency array (`[]`). This results in the effect only running once after the initial mount, potentially leading to stale closure values and unexpected behavior.

The `bugSolution.js` file shows the corrected implementation.  By including `count` in the dependency array (`[count]`), the effect runs whenever `count` changes, ensuring that the logged value is always up-to-date.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install` to install necessary dependencies.
4. Run `npm start` to run the React application.
5. Observe the behavior in the console and compare it to the corrected version.