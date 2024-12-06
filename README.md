# React Native FlatList Performance Issue

This repository demonstrates a common performance issue in React Native's FlatList component when dealing with large datasets. The problem stems from the `renderItem` function being called multiple times for the same item, resulting in slow rendering and potential display errors.

The `bug.js` file shows the problematic implementation, while `bugSolution.js` provides a corrected version with an optimized `keyExtractor` function.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app on an emulator or physical device.
4. Observe the performance issues in the initial implementation and the improvement after applying the fix.

## Solution

The key to resolving this issue is to correctly implement the `keyExtractor` function in the `FlatList` component. This function should provide a unique key for each item in your dataset, ensuring that React Native can efficiently update the list. 