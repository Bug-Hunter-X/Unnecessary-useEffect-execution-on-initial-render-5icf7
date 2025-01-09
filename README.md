# Unnecessary useEffect Execution on Initial Render in React

This repository demonstrates a common issue in React applications where the `useEffect` hook executes on the initial render, leading to unnecessary side effects or console logs.

## The Problem

The provided `MyComponent` uses `useEffect` to log the current count.  While the dependency array `[count]` aims to limit execution to changes in `count`, the effect still runs on the initial render, even though `count` hasn't changed yet.

## The Solution

The solution lies in adding a check inside the `useEffect` to handle the initial render separately or to add a second dependency to account for the initial mount.