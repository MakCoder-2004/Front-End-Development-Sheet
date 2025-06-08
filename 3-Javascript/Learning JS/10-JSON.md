# JSON (JavaScript Object Notation)

```javascript
/*
    - All properties and values must be in double quotes "".
    - JSON is universal, used for data exchange between systems.
    - Used for storing and sending data.
    - Does not support functions.
    - JSON is a string data type.
*/

// Converting an object to JSON
const jsonString = JSON.stringify(person);
console.log(typeof jsonString); // "string"

// Converting JSON back to an object
const jsonObject = JSON.parse(jsonString);
console.log(typeof jsonObject); // "object"
```

---

# Local Storage

```javascript
/*
    - Local Storage allows you to save data in the browser.
    - Only strings can be stored, so objects must be converted to JSON.
*/

// Saving object to local storage (after converting to JSON)
localStorage.setItem("person", JSON.stringify(person));

// Retrieving object from local storage (and converting back to an object)
const storedPerson = JSON.parse(localStorage.getItem("person"));

// Removing an item from local storage
localStorage.removeItem("person");
```

---

This guide demonstrates how to convert objects to JSON, work with JSON strings, and utilize browser local storage to persist data.
