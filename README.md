# React UseEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by incorrect usage of the `useEffect` hook.  The example showcases how updating state within an effect's callback without proper conditionals can lead to unintended behavior and performance issues.

## Bug Description:
The component uses the `useEffect` hook to log a message when the count exceeds 5. It resets the count to 0, which triggers another render and restarts the loop. 

## Solution:
The solution uses conditional rendering and prevents updating the count if it is already less than or equal to 5.