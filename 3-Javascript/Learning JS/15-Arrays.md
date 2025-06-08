# Arrays

```javascript
const elements = [1,2,3,4,5];   ### Type of Arrays are object 
```

### add an element to the end of the array
```javascript
elements.push(6);
```

### remove an element from the end of the array
```javascript
elements.pop();
```

### add an element to the beginning of the array
```javascript
elements.unshift(0);
```

### remove an element from the beginning of the array
```javascript
elements.shift();
```

### get the length of the array
```javascript
const length = elements.length;
```

### get the element at a specific index
```javascript
const elementAtIndex = elements[2];
```

### update the element at a specific index
```javascript
elements[2] = 7;
```

### check if an element exists in the array
```javascript
const exists = elements.includes(5);
```

### find the index of an element in the array
```javascript
const index = elements.indexOf(5);
```

### remove an element by its index
```javascript
const removed = elements.splice(0,1);   // splice(index that is wanted to be removed, no of elements to be removed from the starting index)
```

### remove an element by its value
```javascript
const indexToRemove = elements.indexOf(5);
if (indexToRemove > -1) {
    elements.splice(indexToRemove, 1);
}
```

### sort the array in ascending order
```javascript
elements.sort((a, b) => a - b);
```

### sort the array in descending order
```javascript
elements.sort((a, b) => b - a);
```

### reverse the array
```javascript
elements.reverse();
```

### filter the array
```javascript
const filteredElements = elements.filter(element => element % 2 === 0);
```

### map the array
```javascript
const mappedElements = elements.map(element => element * 2);
```

### some => returns a boolean value
```javascript
const hasEven = elements.some(element => element % 2 === 0);    ### returns true if an even number is found
```

### reduce the array -> reduce the array to a single value
```javascript
const sum = elements.reduce((previous, next) => previous + next, 0/* initial value */); ###sum of the array
```

### slice array (copy the array elements into a new space )
```javascript
const slicedElements = elements.slice(1);
```

---