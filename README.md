# React useEffect Hook Runs Only Once with Empty Dependency Array
This repository demonstrates a common issue with the React `useEffect` hook where an empty dependency array leads to the effect running only once, on mount.  This can be unexpected behavior if you need the effect to run on every state change.

## Problem
The provided `MyComponent` uses `useEffect` with an empty dependency array (`[]`).  This means the effect within the `useEffect` only executes once when the component mounts.  This might cause unexpected issues if one needs the effect to run on every render or state update.

## Solution
To resolve this, include the relevant state variable(s) in the dependency array. In this case, if you want the effect to run every time `count` changes, add `count` to the dependency array.