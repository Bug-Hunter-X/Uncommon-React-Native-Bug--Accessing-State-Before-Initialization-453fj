# Uncommon React Native Bug: Accessing State Before Initialization

This repository demonstrates a common yet easily overlooked bug in React Native: attempting to access a state variable before it has been initialized.  This typically occurs within functional components using the `useState` hook.

## The Problem
The `useState` hook initializes a state variable asynchronously. If you attempt to access this variable before the component's initial render, it will be undefined, leading to errors or unexpected behavior.  The `bug.js` file showcases this problem.

## The Solution
The solution involves ensuring that the state variable is only accessed after it has been properly initialized by the `useState` hook. This can be achieved using conditional rendering or other techniques, as demonstrated in the `bugSolution.js` file.  This involves checking if `count` is defined before using it in the `incrementCount` function and using the initial state value during the initial render.

## How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npx react-native run-android` or `npx react-native run-ios` to run the app on an emulator or device.