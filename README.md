# Unnecessary Re-renders in React Component

This repository demonstrates a common performance issue in React applications: unnecessary re-renders caused by an effect that runs on every render.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The original component uses `useEffect` without dependencies. This causes the effect to run after every render, leading to performance issues and potentially unwanted side effects.  In this specific case, it causes excessive logging to the console.

## Solution

The solution in `bugSolution.js` adds an empty dependency array `[]` to the `useEffect` hook.  This ensures the effect only runs once after the initial render, significantly improving performance.