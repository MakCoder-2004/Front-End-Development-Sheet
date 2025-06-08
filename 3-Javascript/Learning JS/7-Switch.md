# Using the `switch` Statement

A demonstration of using the `switch` conditional structure in JavaScript.

```javascript
var grade = "A";

switch (grade) {
    case "A":
        console.log("Excellent");
        break;
    case "B":
        console.log("Good");
        break;
    case "C":
        console.log("Average");
        break;
    default:
        console.log("Fail");
}
```

---

The `switch` statement is useful for handling multiple possible values of a single variable in a cleaner and more readable way than long chains of `if-else` statements.
