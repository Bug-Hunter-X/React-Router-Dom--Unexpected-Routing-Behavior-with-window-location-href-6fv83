# React Router Dom: Unexpected Routing Behavior with window.location.href

This repository demonstrates a common error in React Router Dom v6 where using `window.location.href` for navigation can cause unexpected behavior and lead to issues with React Router's internal state management.  The `bug.js` file shows the problematic code, while `bugSolution.js` offers the corrected solution.

## Problem

Using `window.location.href` to navigate between routes bypasses React Router's internal routing mechanisms.  This can lead to issues with:

* **State Management:**  React Router manages component state during navigation.  Bypassing this can result in data loss or unexpected state changes.
* **Navigation History:**  The browser's history stack isn't properly updated, potentially breaking the browser's back/forward buttons.
* **Nested Routes:** Can cause problems with nested route parameters and management.

## Solution

The correct way to navigate in React Router Dom is to use the navigation functions provided by the library (e.g., `useNavigate`, `Navigate`, `Link`).  This maintains proper state management and interaction with the routing history.