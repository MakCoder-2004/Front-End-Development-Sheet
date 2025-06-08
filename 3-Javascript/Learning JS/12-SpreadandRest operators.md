# Spread Operator
- Spreads elements of an iterable (like an array or string) into individual elements.
- Can be used with arrays, strings, objects, and more.
- Commonly used in function calls, array literals, and destructuring.


## Getting the minimum from an array
```javascript
const arr1 = [1, 2, 3];
// let minimum = Math.min(arr1); // Error: argument is not a list of numbers
console.log(Math.min(...arr1)); // 1
```

## Spreading a string into an array of characters
```javascript
let name = "Makrious";
let letters = [...name];
console.log(letters); // [ 'M', 'a', 'k', 'r', 'i', 'o', 'u', 's' ]
```

## Combining two arrays
```javascript
let arr2 = [4, 5, 6];
let combinedArray = [...arr1, ...arr2];
console.log(combinedArray); // [1, 2, 3, 4, 5, 6]
```

## Copying an array
```javascript
let arr3 = [...arr1];
console.log(arr3); // [1, 2, 3]
```

---

# Rest Operator (the opposite of spread)
- Collects multiple elements into an array.
- Used in function parameters, destructuring assignments, and more.
- Captures "the rest" of the elements that are not individually picked.

```javascript
let food1 = 'pasta';
let food2 = 'pizza';
let food3 = 'burger';

function fridge(...foods) {
    console.log(foods);
}
fridge(food1, food2, food3); // [ 'pasta', 'pizza', 'burger' ]

function sum(...numbers) {
    let result = 0;
    numbers.forEach(num => {
        result += num;
    });
    return result;
}
console.log(sum(1,2,3,4,5,6,7,8,9,10)); // 55
```

---