# React Router Dom v6 Catch All Route Not Working

This repository demonstrates a common issue encountered when using the catch-all route (*) in React Router Dom v6.  The catch-all route, intended to handle any unmatched paths, unexpectedly fails to render the designated component (NotFound in this example).

## Problem

The provided code uses React Router v6 and includes a catch-all route (`path="*"`). However, when navigating to a non-existent route, the `NotFound` component doesn't render as expected. The issue stems from how the router handles routes and the context they operate in. The solution improves how routes interact in React Router v6.

## Solution

The solution involves ensuring the catch-all route is placed correctly within the `Routes` component to prioritize other routes before redirecting to the 404 page.  The changes ensure the catch-all route only triggers if none of the other routes match the current URL.