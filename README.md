# Stale Closure in React Functional Component State Update

This repository demonstrates a common issue in React functional components related to stale closures when updating state.  The problem arises when a function that relies on the state value uses the previous value of the state variable instead of the most recent one, leading to unexpected behavior or incorrect updates.

## Bug Description
The provided code uses a closure (`count`) within the `incrementCount` function. In scenarios of asynchronous updates or multiple updates occurring quickly, the closure value might be outdated, resulting in incorrect updates.

## Solution
The solution uses functional updates with `setCount` to ensure that the state update always uses the latest value of `count`.