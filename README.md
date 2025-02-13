# React Native Dimensions API returns 0 or undefined on initial render

This repository demonstrates a common issue when using the `Dimensions` API in React Native: getting `0` or `undefined` for screen dimensions on initial component render.  This happens because the dimensions are not available synchronously.

## Problem

When accessing `Dimensions.get('window')` directly in a component, the values might not be ready. This leads to incorrect layout calculations or unexpected behavior.

## Solution

The solution involves using the `Dimensions` API asynchronously, typically using `useEffect` hook to ensure the dimensions are fetched after the component mounts and the layout is calculated.