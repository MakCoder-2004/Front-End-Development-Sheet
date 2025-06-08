# JavaScript Objects

An overview of objects, including properties, methods, and key operations.

```javascript
// Defining an object
const person = {
    name: "John",
    age: 30,

    // Nested object
    location: {
        country: "USA",
        city: "New York"
    },

    // Method
    greet: function() {
        console.log("Hello, " + person.name);
    }
};

console.log(person);
console.log(person.location.city);
person.greet(); // Hello, John

// Accessing properties
console.log(person.name); // John
console.log(person["age"]); // 30

// Updating properties
person.age = 31;
console.log(person);

// Deleting a property
delete person.age;
console.log(person);

// Adding a new property
person.Married = false;
console.log(person);

// Checking for property existence
console.log("name" in person); // true
console.log("email" in person); // false

// Referencing (object references)
const person2 = person;
console.log(person2 === person); // true
```

## Object Destructuring

```javascript
const { age } = person;
console.log(age);
```

## The `this` Keyword

### Incorrect usage:
```javascript
const person = {
    name: "Makrious",
    age: 30,
    greet: function() {
        console.log("Hello, " + name); // Error: 'name' is not defined in this scope
    }
};
```

### Correct usage with `this`:
```javascript
const person1 = {
    name: "John",
    age: 30,
    greet: function() {
        console.log("Hello, " + this.name); // Correct: refers to person1.name
    }
};
```

---

This file demonstrates how to work with JavaScript objects: defining, accessing, modifying, and using methods, along with key concepts like destructuring, referencing, and `this`.