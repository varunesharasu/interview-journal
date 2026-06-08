| Feature         | `var`             | `let`        | `const`      |
| --------------- | ----------------- | ------------ | ------------ |
| Scope           | Function scoped   | Block scoped | Block scoped |
| Re-declaration  | Allowed           | Not allowed  | Not allowed  |
| Re-assignment   | Allowed           | Allowed      | Not allowed  |
| Hoisted         | Yes (`undefined`) | Yes (TDZ)    | Yes (TDZ)    |
| Preferred Today | Rarely            | Yes          | Yes          |


### var is function-scoped and allows re-declaration and re-assignment. let is block-scoped, allows re-assignment but not re-declaration. const is block-scoped and allows neither re-declaration nor re-assignment. In modern JavaScript, let and const are preferred over var because they provide better scope control and avoid common bugs.
