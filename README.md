# Inconsistent Dimensions on Android

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native on Android. The problem is that the dimensions returned by `Dimensions.get('window')` can be incorrect (e.g., 0, undefined) during the initial render or after a screen rotation.

## Problem

The provided `bug.js` demonstrates a simple component using `Dimensions` to set the width and height of a view. On Android, this often results in the view initially rendering with incorrect dimensions or even being invisible due to `undefined` values.

## Solution

The solution involves using the `Dimensions` API with the `useEffect` hook and ensuring that the layout has been measured before accessing the dimensions. `bugSolution.js` showcases this correct usage, guaranteeing that the dimensions are accurately reflected in the component's layout.

## How to Reproduce

1. Clone this repository.
2. `cd` into the project directory.
3. Run `npx react-native run-android`.
4. Observe the behavior of the initial render on an Android device.
5. Rotate the screen, and observe the effect on the displayed view.