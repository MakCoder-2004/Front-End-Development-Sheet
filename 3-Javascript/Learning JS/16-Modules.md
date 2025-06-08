# JavaScript Modules and Date Handling

## Modules

### Enabling Modules in HTML

To use ES Modules, add the `type="module"` attribute to your `<script>` tag in the HTML:

```html
<script type="module" src="./script1.js"></script>
```

### Importing and Exporting in Modules

#### `script2.js`

```js
export const variable1 = "Hello from script1";
```

#### `script1.js`

```js
import { variable1 as myVar } from "./script2.js";
```

This setup allows you to import/export variables or functions between JavaScript files.

---

## External Libraries

JavaScript allows importing code from external libraries.

### Syntax:

```js
import LibraryName from 'Link-To-The-Library';
```

### Example Libraries

* **Hello (ESM version)**: `https://unpkg.com/supersimpledev@1.0.1/hello.esm.js`
* **DayJS (ESM version)**: `https://unpkg.com/dayjs@1.11.10/esm/index.js`

> ESM (ECMAScript Module) versions help avoid function name collisions by using module encapsulation.

---

## Using the DayJS Library

### Get Today's Date

```js
const today = dayjs();
```

### Format a Date

```js
const formattedDay = today.format('YYYY-MM-DD');
```

[More formatting options](https://day.js.org/)

### Add Days to the Current Date

```js
const add7days = today.add(7, 'day');
```

---

## Native JavaScript `Date` Object

### Get Current Date and Time

```js
const date = new Date();
console.log(date);
```

### Extract Date Components

```js
const year = date.getFullYear();
const month = date.getMonth() + 1; // Months are 0-indexed
const day = date.getDate();
const hour = date.getHours();
const minute = date.getMinutes();
const dayOfTheWeek = date.getDay();
```

### Set the Year

```js
const setYear = date.setFullYear(2004);
```

---