# JavaScript Promises and Async/Await Study Guide

---

## What is a Promise

A **Promise** in JavaScript is an object representing the eventual completion or failure of an asynchronous operation. Promises are used to handle asynchronous operations more effectively than callbacks.

```js
let promise = new Promise((resolve, reject) => {
  // async task
  if (success) {
    resolve('Success!');
  } else {
    reject('Error!');
  }
});
```

---

## Promises in Real Life

This lesson uses real-world analogies (like ordering coffee or online shopping) to explain how Promises behave — they represent something that hasn't happened yet but will in the future.

---

## Promise Constructor

Teaches how to manually create a promise using the `new Promise()` constructor, defining the `resolve` and `reject` functions for success or failure paths.

```js
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Done!"), 1000);
});
```

---

## Promise Object Properties

Covers the internal states of a promise:

* `pending`
* `fulfilled`
* `rejected`

Understanding these helps in tracking the state of asynchronous tasks.

---

## Create Your First Promise

A hands-on guide to creating and resolving a simple promise and handling the result using `.then()`.

---

## Access Fulfilled Promise Data

Learn how to access the data returned from a resolved promise using the `.then()` method.

```js
myPromise.then((data) => console.log(data));
```

---

## Then Method

The `.then()` method registers callbacks to receive either the promise’s eventual value or the reason why it was rejected.

```js
myPromise
  .then(response => console.log(response))
  .catch(error => console.error(error));
```

---

## Using Promises in Depth

Explores chaining multiple `.then()` calls and handling complex asynchronous flows with Promises.

---

## Promises Error Handling

Discusses `.catch()` and how to handle errors in promise chains to prevent unhandled rejections.

```js
fetch('https://api.example.com')
  .then(response => response.json())
  .catch(err => console.error('Failed:', err));
```

---

## Refactor & Finally Method

Introduces the `.finally()` method for running cleanup logic regardless of the promise result.

```js
myPromise.finally(() => console.log("Cleanup done"));
```

---

## Promise.race() Method

Returns a promise that resolves or rejects as soon as one of the promises in the iterable resolves or rejects.

```js
Promise.race([promise1, promise2])
  .then(result => console.log(result));
```

---

## Promise.all() Method

Waits for all promises to resolve and returns a new promise with an array of results. If one fails, the whole operation fails.

```js
Promise.all([promise1, promise2])
  .then(results => console.log(results));
```

---

## Promise.any() Method

Returns the first fulfilled promise, ignoring rejected ones. Fails only if all promises reject.

```js
Promise.any([promise1, promise2])
  .then(result => console.log(result));
```

---

## Intro to Async/Await

Introduces `async` and `await` as syntactic sugar over promises, making asynchronous code look synchronous.

```js
async function fetchData() {
  const response = await fetch('https://api.example.com');
  const data = await response.json();
  console.log(data);
}
```

---

## Convert from Promises to Async/Await

Shows how to refactor `.then()` promise chains to use `async/await` for better readability.

Before:

```js
fetch(url)
  .then(res => res.json())
  .then(data => console.log(data));
```

After:

```js
const data = await (await fetch(url)).json();
console.log(data);
```

---

## Get User Todos

Demonstrates a practical example of using async/await to fetch user data like to-dos from an API.

---

## Error Handling with Try Catch

Covers error handling in async/await using try/catch blocks to gracefully catch and manage errors.

```js
try {
  const data = await fetchSomething();
} catch (error) {
  console.error("Something went wrong", error);
}
```

---
