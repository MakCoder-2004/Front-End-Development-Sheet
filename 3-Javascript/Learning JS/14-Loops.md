# Loop

## for loop
```javascript
for (let i = 0; i < elements.length; i++) {
    console.log(elements[i]);
}
```

---

## for each
```javascript
elements.forEach((values, Index) => {
    console.log(`${Index}: ${values}`);
});
```

- or
  
```javascript
elements.forEach(function(values, Index){
    console.log(`${Index}: ${values}`);
});
```

## example
```javascript
let nums = [1, 2, 3, 4, 5];

function double(element, index, array) {
    array[index] = element * 2;
}

function display(element, index) {
    console.log(index + ':' + element);
}
```

---

## Double the values in the array
```javascript
nums.forEach(double);
```

## Display the updated array
```javascript
nums.forEach(display);
```

---