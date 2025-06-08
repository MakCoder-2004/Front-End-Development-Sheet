## String Functions in JavaScript

---

### String Properties and Methods

* `String.prototype.length` → Get the length of a string
* `String.prototype.toUpperCase()` → Convert a string to uppercase
* `String.prototype.toLowerCase()` → Convert a string to lowercase

### Multi-line Strings

```javascript
var multiLineString2 = `Hello
World

This is a multi-line string`;
```

### Concatenation

```javascript
var name = "John";
var age = 30;

var message = "My name is " + name + " and I am " + age + " years old.";

// Concatenating string and number
var message2 = "My name is " + name + 30; // "My name is John30"
```

### String Interpolation

```javascript
var message3 = `My name is ${name} and I am ${age} years old.`;
```

### Escape Characters

```javascript
var message3 = "Hello \nWorld";   // New line
var message4 = "Hello \tWorld";   // Tab
var message5 = "Hello \"World\""; // Quotes
var message6 = "Hello \bWorld";   // Backspace
```

### Type Checking

* `typeof variable` → Returns the type of a variable

### Type Conversion

```javascript
var myVariable = "Hello World!";
myVariable = Number(myVariable);  // Convert string to number (NaN)

var myVariable2 = 10;
myVariable2 = String(myVariable2);  // Convert number to string
```

### Console Output

```javascript
console.log("Makrious Ayman");
```

---

### Prompting for Input

```javascript
var name = prompt("Enter your name:");
console.log("Hello, " + name);

var age = prompt("Enter your age:");
console.log("You are " + age + " years old.");
```

---
