# React useEffect Infinite Loop Bug
This example demonstrates a common mistake in React's `useEffect` hook that leads to an infinite loop. The problem lies in how the dependency array is handled.

## Problem
The `useEffect` hook is designed to run after every render. However, if the dependency array is incorrect, it can lead to unexpected behavior. In this case, omitting the dependency array (`[]`) or including a value that changes on every render results in an infinite loop.

## Solution
The solution involves correctly specifying the dependency array. If you want the `useEffect` to run only when `count` changes, then `[count]` should be the dependency array.  If you want it to run only once after mount, an empty array `[]` should be used.