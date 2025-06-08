# JavaScript: Synchronous vs Asynchronous Programming

## Synchronous Programming

* Tasks are performed one after the other.
* The program waits for the current task to finish before moving to the next.

```js
console.log("Task 1");
console.log("Task 2");
console.log("Task 3");
```

**Output:**

```
Task 1
Task 2
Task 3
```

## Asynchronous Programming

* Tasks can run independently.
* The program can continue executing other code while waiting for an asynchronous task to complete.

```js
console.log("Task 1");
setTimeout(() => console.log("Task 2 (delayed)"), 2000);
console.log("Task 3");
```

**Output:**

```
Task 1
Task 3
Task 2 (delayed)
```

---

## Callback Functions (Illustration)

A **callback** is a function passed as an argument to another function. It allows one function to run after another is complete.

### Illustrative Example (without async)

```js
function greet(name, callback) {
    console.log("Hello " + name);
    callback();
}

function sayGoodbye() {
    console.log("Goodbye!");
}

greet("Alice", sayGoodbye);
```

**Output:**

```
Hello Alice
Goodbye!
```

---

## Asynchronous Example Using `setTimeout` and Callbacks

```js
function fetchData(callback) {
    console.log("Fetching data...");
    setTimeout(() => {
        console.log("Data fetched!");
        callback();
    }, 3000);
}

function processData() {
    console.log("Processing data...");
}

fetchData(processData);
```

**Expected Output:**

```
Fetching data...
(Data fetched after 3 seconds)
Data fetched!
Processing data...
```

---

### Summary

* **Synchronous:** Code executes step-by-step.
* **Asynchronous:** Code executes without waiting; later tasks can run in the background.
* **Callbacks:** Let you run code *after* an asynchronous operation is finished.

---