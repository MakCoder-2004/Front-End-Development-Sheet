# JavaScript String Methods

A handy collection of common built-in string methods with examples and explanations.

---

## Basic Properties and Access

```javascript
console.log("Hello".length);       // 5 - Number of characters
console.log("Hello".charAt(0));   // 'H' - Character at index 0
```

## Case Conversion
```javascript
console.log("Hello".toUpperCase());  // "HELLO" - Convert to uppercase
console.log("Hello".toLowerCase());  // "hello" - Convert to lowercase
```

## Searching Within Strings
```javascript
console.log("Hello".indexOf("l"));       // 2 - First occurrence of 'l'
console.log("Hello".lastIndexOf("l"));   // 3 - Last occurrence of 'l'
console.log("Hello, World".includes("World"));  // true - Substring exists?
console.log("Hello, World".startsWith("Hello")); // true - Starts with?
console.log("Hello, World".endsWith("World"));   // true - Ends with?
```

## Splitting and Extracting
```javascript
console.log("Hello".split(""));          // ["H", "e", "l", "l", "o"] - Split into characters
console.log("Hello World".split(" "));   // ["Hello", "World"] - Split into words
console.log("Hello, World".slice(0, 5)); // "Hello" - Extract portion (supports negative indices)
console.log("Hello, World".substring(0, 5)); // "Hello" - Extract portion (no negative indices)
```

## Modifying Strings
```javascript
console.log("Hello, World".replace("Hello", "Hi"));   // "Hi, World" - Replace substring
console.log("Hello, World".concat("!"));               // "Hello, World!" - Concatenate strings
console.log("  Hello, World  ".trim());                // "Hello, World" - Remove whitespace
console.log("Hello, World\n".repeat(3));               // Repeats string 3 times
```

## Padding
```javascript
console.log("Hello, World".padStart(15, "0")); // "0000Hello, World" - Pad at start
console.log("Hello, World".padEnd(15, "0"));   // "Hello, World0000" - Pad at end
```

---