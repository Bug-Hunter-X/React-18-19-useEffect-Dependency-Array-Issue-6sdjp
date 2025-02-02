# React useEffect Dependency Array Issue

This repository demonstrates a common issue encountered in React 18 and 19 related to the `useEffect` hook's dependency array.  Improperly specifying dependencies can lead to unexpected behavior and bugs.

The `bug.js` file contains code with a missing dependency in the useEffect hook.  This causes the effect to not update correctly when the `count` state changes. The `bugSolution.js` file shows the corrected code. 

## How to reproduce

1. Clone this repository.
2. Navigate to the directory containing the bug.js and bugSolution.js files.
3. Run `npm install` to install dependencies (assuming you have node and npm installed).
4. Run `npm start` (if you create a simple react app).
5. Observe the behavior of both versions of the component.

## Solution

The solution involves correctly specifying the dependencies of the `useEffect` hook.  In this example, the `count` variable should be included in the dependency array. By including `count` the effect will re-run whenever the value of `count` changes.  This ensures that the effect always uses the latest value of `count`. 