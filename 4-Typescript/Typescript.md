# TypeScript Guide Sheet

TypeScript is a strongly typed superset of JavaScript that adds static typing to JavaScript.

---

## Common Usages of TypeScript

* **Web Development**: Used in frameworks like Angular, React, and Vue for scalable applications.
* **Backend Development**: Works with Node.js for building APIs and services.

**By:** Makrious Ayman
[LinkedIn](https://www.linkedin.com/in/makrious-ayman-84985621b/)

**Source:**

* TS documentation
* [freeCodeCamp YouTube Course](https://www.youtube.com/watch?v=30LWjhZzg50&t=2361s)

---

## Steps to Initialize TypeScript Using Yarn

1. `yarn add typescript ts-node -g`
   Creates `tsconfig.json` in dependencies.
2. `yarn remove typescript ts-node`
   Removes from `package.json`.
3. `yarn add typescript ts-node -D`
   Adds to `devDependencies`.
4. `npx ts-node TypescriptFile.ts`
   Executes the file.
5. `npx tsc TypescriptFile.ts`
   Compiles `.ts` file to `.js`.
6. `tsc TypescriptFile.ts -w`
   Watch mode for automatic recompile.
7. `tsc --init`
   Creates `tsconfig.json`.
8. Change `rootDir` to your TS source folder.
9. Change `outDir` to your JS output folder.

---

## Type Annotations & Inference

* `let name: string = "Makrious";`
* Inference: `let age = 20;` (TypeScript knows it's a number)

### Primitive Types

* `string`
* `number`
* `boolean`
* `any` *(Avoid using this)*

---

## Functions

```ts
let login = (name: string, password: string, isAdmin: boolean = false) => {
    console.log(`Welcome ${name}!`);
};

function addTwo(number: number) {
    return number + 2;
}

function displayProduct(): void {
    console.log("This is a displayProduct function");
}

function addOne(number: number): {} {
    return number + 1;
}

function HandleEError(err: string): never {
    throw new Error(err);
}
```

---

## Objects and Destructuring

```ts
const user = {
    name: "Makrious",
    age: 20,
    isMarried: false,
    sayHello() {
        return 'Hello !';
    }
};

const user2: {
    name: string,
    age: number,
    isMarried: boolean
} = user;
```

### Spread Operator

```ts
const person2 = { ...person, address: "Alexandria" };
```

---

## Type Aliases

```ts
type Person = {
    name: string,
    age: number,
    isMarried: boolean
};
```

---

## Interfaces

```ts
interface Citizen {
    readonly _id: number;
    name: string;
    age: number;
    isMarried: boolean;
    greeting(): string;
    getLicence(carNumber: number): number;
    nationality?: string;
}
```

---

## Readonly

Prevents modification:

```ts
readonly _id: number;
```

---

## Optional Properties

```ts
credirCard?: number;
```

---

## Combining Types

```ts
type creditCardDetails = credirCardNumbers & credirCardDate & {
    name: string,
    age: number,
    isMarried: boolean
};
```

---

## Arrays and Tuples

```ts
const SuperHeros: string[] = [];
type man = [string, number];
```

---

## Union Types

```ts
let money: number | string;
let pet: dog | cat;
```

---

## keyof Operator

```ts
type personKeys = keyof Person2;
```

---

## Enums

```ts
const enum Payment {
    VISA,
    MasterCard,
    PayPal,
}
```

---

## Object-Oriented Programming (OOP)

### Class

```ts
class Student {
    constructor(private _id: number) {}

    get id(): number {
        return this._id;
    }

    set id(value: number) {
        if(value > 0) this._id = value;
        else throw new Error("ID must be positive");
    }
}
```

### Abstract Class

```ts
abstract class TakePhoto {
    constructor(public cameraMode: string, public filter: string, public iso: number) {}
    abstract displayinfo(): void;
}
```

---

## Record Utility

```ts
const person4: Record<string, string | number> = {
    name: "Makrious",
    age: 20
};
```

---

## Generics

```ts
function genericIdentity<T>(val: T): T {
    return val;
}
```

---

## Partial

```ts
function updatePerson(person: Person5, updates: Partial<Person5>) {
    return { ...person, ...updates };
}
```

---

## Index Signatures

```ts
interface cities {
    [key: number]: string;
}
```

---

## Type Narrowing

```ts
function typeNarrowing(val: number | string) {
    if (typeof val === 'string') return val.toLowerCase();
    return val.toFixed(2);
}
```

---

## Synchronous vs Asynchronous

* **Synchronous**: Tasks are executed one after another.
* **Asynchronous**: Tasks can execute independently using callbacks, promises, or async/await.

```ts
function getToTodoList(callback: () => void) {
    setTimeout(() => {
        todoList = [{ id: 1, task: "Task 1" }];
        callback();
    }, 5000);
}
```

---