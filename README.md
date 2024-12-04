# React 19 useEffect Hook Bug
This repository demonstrates a common bug in React 19 related to the `useEffect` hook.  The bug occurs when a state variable is used within the `useEffect` function but is not included in the dependency array, leading to an infinite rendering loop.

## Bug Description
The `MyComponent` uses `useState` to manage a count.  The `useEffect` hook is intended to log the count after each render.  However, because `count` is not listed in the dependency array, the effect runs after every render, causing an infinite loop.

## Solution
The solution is simply to add `count` to the dependency array. This ensures that the effect only runs when `count` changes.

## How to Reproduce
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite console logs and browser performance issues.