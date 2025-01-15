# React useState Hook Unexpected Behavior with Functional Updates

This repository demonstrates a subtle bug related to the use of functional updates within the `useState` hook in React. The bug manifests when attempting to update the state twice within a single event handler, resulting in unexpected and inconsistent state updates.

## Bug Description
The primary issue arises from the way React batches state updates. When calling `setCount` multiple times within a single event handler, React's batching optimization might lead to only the last update being applied, potentially skipping intermediate updates.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the increment behavior in the component.  Notice that the counter does not increment by two each time, as expected.

## Solution
The solution involves ensuring that the state update is correctly handled, preventing the loss of any intended updates.
