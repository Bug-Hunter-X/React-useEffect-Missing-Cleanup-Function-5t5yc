# React useEffect Missing Cleanup Function
This repository demonstrates a common error in React applications involving the `useEffect` hook. Specifically, it showcases a scenario where the cleanup function is omitted, potentially leading to memory leaks or unexpected behavior.

## Problem
The `useEffect` hook is used to perform side effects in functional components.  When a cleanup function is needed (e.g., to cancel subscriptions or timers), it should be returned from the `useEffect` callback.  Failure to return a cleanup function can result in unexpected behavior and memory leaks if the component unmounts before the side effects have completed.

## Solution
The solution involves adding a cleanup function to the `useEffect` hook. This function will execute when the component unmounts, ensuring that any resources used by the side effect are released.

## How to run the example
1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.