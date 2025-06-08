## Boolean Values in JavaScript

---

### Boolean Basics

```javascript
var isTrue = true;      // true
var isFalse = false;    // false
```

### Comparison Operators

* `==` compares values after type conversion (loose equality)
* `===` compares both value and type (strict equality)

```javascript
console.log(5 == "5.00");    // true (value comparison)
console.log(5 === "5.00");   // false (type + value comparison)
```

### Not Equal Operators

* `!=` checks for inequality with type conversion
* `!==` checks for inequality without type conversion

```javascript
console.log(5 != "5.00");     // false
console.log(5 !== "5.00");    // true
```

---