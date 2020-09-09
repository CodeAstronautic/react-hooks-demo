# react-hooks-demo


Hooks are functions that let you “hook into” React state and lifecycle features from function components. 
Hooks don’t work inside classes — they let you use React without classes.


⚡️ Effect Hook
You’ve likely performed data fetching, subscriptions, or manually changing the DOM from React components before.
We call these operations “side effects” (or “effects” for short) because they can affect other components and can’t be done during rendering.

The Effect Hook, useEffect, adds the ability to perform side effects from a function component.
It serves the same purpose as componentDidMount, componentDidUpdate, and componentWillUnmount in React classes, but unified into a single API.

(We’ll show examples comparing useEffect to these methods in Using the Effect Hook.)

# for Example

import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
