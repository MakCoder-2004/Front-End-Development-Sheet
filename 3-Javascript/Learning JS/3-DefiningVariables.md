## Defining Variables in JavaScript

---

### Declaring Variables

```javascript
var myVariable = "Hello World!";  // declare and initialize a variable
let name = "Makrious";            // block-scoped variable
```

### Differences between `var` and `let`

| Feature         | var                                  | let                            |
| --------------- | ------------------------------------ | ------------------------------ |
| Scope           | Function-scoped                      | Block-scoped                   |
| Hoisting        | Hoisted (initialized as `undefined`) | Hoisted (TDZ: not initialized) |
| Re-declaration  | Allowed                              | Not allowed                    |
| Global Property | Added to `window` (in browsers)      | Not added to `window`          |

**Use `let` for block-scoping and safer behavior.**
**Use `var` only for function-scoping or legacy code.**

### Scope Example

```javascript
if (true) {
    var x = 10; // Function-scoped (or globally scoped if not in a function)
    let y = 20; // Block-scoped
}
console.log(x); // 10 (accessible)
console.log(y); // ReferenceError: y is not defined
```

### Hoisting Example

```javascript
console.log(a); // undefined (hoisted but not initialized)
var a = 5;

console.log(b); // ReferenceError: Cannot access 'b' before initialization
let b = 10;
```

### Re-declaration Example

```javascript
var x = 10;
var x = 20; // No error

let y = 10;
// let y = 20; // SyntaxError: Identifier 'y' has already been declared
```

### Constants

```javascript
const PI = 3.14; // Value cannot be changed
```

---
