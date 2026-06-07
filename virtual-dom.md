When something changes in React (like state):

State changes
React re-runs the component function
A new Virtual DOM is created
React compares (Diffing) old vs new Virtual DOM
Only the changed parts are sent to the Real DOM
Real DOM updates the UI
❗ Key clarification (important)

It’s not that the “first change happens only in Virtual DOM” like a separate place.

Instead:

The component re-executes → which recreates the Virtual DOM representation → then React calculates changes.

So technically:

There is no direct mutation in Virtual DOM
A new Virtual DOM tree is created every render
🧠 Simple correct mental model
State Change
   ↓
Component re-renders
   ↓
New Virtual DOM created
   ↓
Diff with previous Virtual DOM
   ↓
Real DOM updates (only differences)
⚡ Important insight (interview point)
Virtual DOM is not a real DOM in memory that gets updated
It is just a JavaScript object representation created every render
React uses it to decide what to update in the real DOM
