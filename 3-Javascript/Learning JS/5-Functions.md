## JavaScript Functions Cheat Sheet

### Function Declaration (Hoisted)
```javascript
function greet(name) {
    console.log("Hello, " + name);
}
greet("John");
```

### Function Expression (Not Hoisted)
```javascript
const greetFunction = function(name) {
    console.log("Hello, " + name);
}
console.log(greetFunction("Makrious"));
```

---

### setTimeout Function
- Executes a function after a specified delay (in milliseconds).
- Non-blocking: it sets the timer and proceeds immediately to the next line.

```javascript
const setTimeoutFunc = setTimeout(function() {
    console.log("Hello from setTimeout");
}, 2000);

clearTimeout(setTimeoutFunc); // Cancels the timeout if called before execution
```

---

### setInterval Function
- Repeatedly calls a function every X milliseconds.

```javascript
let func = setInterval(function() {
    console.log("Hello from setInterval");
}, 3000);

clearInterval(func); // Stops the repeated execution
```

---

### Arrow Functions
#### Syntax:
```javascript
let arrowFunction = () => {
    console.log("This is an arrow function");
}
arrowFunction();

let multiply = (a, b) => a * b;
console.log(multiply(5, 7)); // Output: 35
```

---