# If Statements vs. Ternary Operator

A demonstration of using conditional statements in JavaScript.

---

## Using `if-else` Statements

```javascript
var age = 25;

if (age >= 18) {
    console.log("You are an adult");
} else if (age === 0) {
    console.log("Invalid age");
} else {
    console.log("You are a child");
}
```

---

## Using the Ternary Operator

The ternary operator provides a concise way to write simple `if-else` logic.

```javascript
//       condition        ?      if true         :       if false
var isAdult = age >= 18 ? "You are an adult" : "You are a child";
console.log(isAdult);
```

---