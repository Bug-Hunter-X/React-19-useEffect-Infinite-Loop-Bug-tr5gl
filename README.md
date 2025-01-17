# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common, yet subtle, bug in React 19 involving the `useEffect` hook.  The bug arises from incorrectly using the state variable within the `useEffect`'s dependency array, leading to an infinite rerendering loop. The solution showcases a proper way to manage state updates within `useEffect` to avoid this issue. 

## Bug Description
The bug involves attempting to update a state variable directly within a `useEffect` hook without properly managing the dependencies. This can easily lead to an infinite loop, particularly if the state is accessed and updated concurrently inside the effect, resulting in continuous re-renders.

## How to Reproduce
1. Clone the repository.
2. Run `npm install`
3. Run `npm start`

The application will render, and the console will log continuous updates.