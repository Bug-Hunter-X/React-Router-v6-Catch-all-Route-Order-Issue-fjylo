# React Router v6 Catch-all Route Order Issue

This repository demonstrates a common issue encountered when using catch-all routes (`path="*"`) in React Router v6.  The problem arises when the catch-all route is not placed as the last route within the `Routes` component.  This leads to the catch-all route unintentionally intercepting other routes, resulting in unexpected behavior and preventing other routes from being matched correctly.

## Bug Description

The bug occurs because the order of routes matters in `react-router-dom`.  If a catch-all route is placed before other specific routes, it will always match first, even if there is a more specific route that should be matched. 

## Solution

The solution is simple.  Always place your catch-all route (`path="*"`) as the last route defined within the `Routes` component. This ensures that it will only be matched if none of the preceding routes match the URL.