# React Native useEffect Async Operations and Cleanup

This repository demonstrates a common issue in React Native applications related to the use of the `useEffect` hook with asynchronous operations. Specifically, it highlights the importance of proper cleanup functions to prevent errors when a component unmounts before an asynchronous operation completes.

## Problem

The `bug.js` file shows an example of how an asynchronous operation inside `useEffect` can lead to unexpected behavior. The problem is that if the component unmounts before the asynchronous operation finishes, attempting to update state might throw warnings or errors.

## Solution

The `bugSolution.js` file provides a solution that addresses the issue by using a cleanup function to cancel the asynchronous operation if the component unmounts. This approach ensures that the component doesn't try to update state after it has been unmounted.