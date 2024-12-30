# React setInterval Memory Leak

This repository demonstrates a common mistake in React components: using `setInterval` within a `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Problem

The `bug.js` file contains a component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts. This means that the interval continues to run even after the component is no longer displayed, leading to a memory leak.

## Solution

The `bugSolution.js` file shows the corrected component. It uses the return value of `useEffect` to clear the interval before the component unmounts. This prevents memory leaks and ensures proper behavior.

## How to reproduce

1. Clone this repository
2. Run `npm install`
3. Run `npm start`