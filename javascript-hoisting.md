what is hoisting in js

Hoisting in JavaScript means that variable and function declarations are moved to the top of their scope before the code runs.

Example with var
console.log(name);
var name = "John";

JavaScript treats it roughly like:

var name;
console.log(name);
name = "John";

Output:

undefined
