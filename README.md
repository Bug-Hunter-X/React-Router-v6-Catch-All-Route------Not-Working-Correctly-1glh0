# React Router v6 Catch-All Route Issue

This repository demonstrates a bug in React Router v6 where the catch-all route (`/*`) doesn't function correctly.  The catch-all route should only be triggered when no other routes match, but in this example, it's always activated, even when other paths are valid.

## Setup

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.

## Problem

Navigate to `/` or `/about`. The `NotFound` component should only appear when accessing an invalid URL, but it displays regardless.  This issue prevents proper route handling. 

## Solution

The solution involves correctly ordering the routes. The catch-all route should be placed as the last route in the `Routes` component.