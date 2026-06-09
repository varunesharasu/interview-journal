types of import and export statement in js

JavaScript mainly has 2 types of exports and corresponding imports.

1. Named Export
Export
export const name = "John";

export function greet() {
    console.log("Hello");
}
Import
import { name, greet } from "./file";

Important: Names must match exactly.

2. Default Export

A file can have only one default export.

Export
export default function greet() {
    console.log("Hello");
}
Import
import greet from "./file";

You can choose any name:

import myFunction from "./file";
Named + Default Together
file.js
export const age = 25;

export default function greet() {
    console.log("Hello");
}
Import
import greet, { age } from "./file";
Import All (*)

Import everything from a file.

Export
export const name = "John";
export const age = 25;
Import
import * as user from "./file";

console.log(user.name);
console.log(user.age);
Alias Import (as)

Rename imported items.

Export
export const name = "John";
Import
import { name as userName } from "./file";
Side-Effect Import

Used when you only want the file to execute.

import "./styles.css";

Common in React for:

CSS files
Configuration files
Polyfills

| Type            | Export                 | Import                              |
| --------------- | ---------------------- | ----------------------------------- |
| Named Export    | `export const a = 10`  | `import { a } from "./file"`        |
| Default Export  | `export default greet` | `import greet from "./file"`        |
| Named + Default | Both together          | `import greet, { a } from "./file"` |
| Import All      | Multiple exports       | `import * as obj from "./file"`     |
| Alias           | `export const a`       | `import { a as b } from "./file"`   |
| Side Effect     | Any file               | `import "./file"`                   |



# import React from "react";           // Default import

# import { useState } from "react";    // Named import

# import React, { useState } from "react"; // Both
