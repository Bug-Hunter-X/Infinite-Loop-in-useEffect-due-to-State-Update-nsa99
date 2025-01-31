# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by updating state within a useEffect hook without proper dependency management.

## The Problem

The `useEffect` hook in `bug.js` runs after every render.  The `setCount` function updates the `count` state, triggering a re-render.  This leads to the `useEffect` hook running again, creating an infinite loop and causing the console to be flooded with log messages.

## The Solution

The solution, in `bugSolution.js`, uses the `count` state as a dependency for the `useEffect` hook.  This ensures that the effect only runs when the `count` state changes and prevents the infinite loop.