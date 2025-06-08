# JavaScript Destructuring

Destructuring allows you to unpack values from arrays or properties from objects into distinct variables, making code cleaner and more readable.

---

## Syntax

* **Array Destructuring**: `[]`
* **Object Destructuring**: `{}`

---

## Example 1: Array Destructuring

```js
let a = 1;
let d = 2;

[a, d] = [d, a]; // Swap values

console.log(a); // 2
console.log(d); // 1
```

---

## Example 2: Object Destructuring in Function Parameters

```js
const person3 = {
    name: "John",
    age: 30,
    city: "New York"
};

const person4 = {
    name: "Mark",
    age: 30
};

function displayPerson({name, age, city="Not Stated"}) {
    console.log(`Name: ${name}\n Age: ${age}\n City: ${city}`);
}

displayPerson(person3); // City: New York
displayPerson(person4); // City: Not Stated
```

---

## Example 3: Using Rest Parameters and Custom Class

```js
class Student {
    constructor(name, age, ...address) {
        this.name = name;
        this.age = age;
        this.address = new Address(...address);
    }
}

class Address {
    constructor(street, city, state) {
        this.street = street;
        this.city = city;
        this.state = state;
    }
}

const student1 = new Student("John", 30, "123 Main St", "New York", "NY");
```

---