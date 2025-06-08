# DOM (Document Object Model)

```bash
    document
            ---> <html>
                    |---> <head>
                    |           |---> <title>
                    |
                    |---> <body>
                                |---> elements....
```           

## Element Selectors

### change body content
```javascript
document.body.innerHTML = "This is a new page!";
```
---

### change title
```javascript
document.title = "New Page Title";
```
---

## query selector => returns the first matching element

### select the first selector needed
```javascript
document.querySelector('button');
```

### select the content of the typed selector
```javascript
document.querySelector('button').innerHTML;
```

### select element by its id
```javascript
document.querySelector('#idName ');
```

### select element by its class
```javascript
document.querySelector('.ClassName'); 
```

---

## query selector all => returns the matching elements as an array
```javascript

const elementsByQuery = document.querySelectorAll('li');
console.log(elementsByQuery[2]);
```

### select elements by their class
```javascript
const elementsByClass = document.getElementsByClassName('className');
console.log(elementsByClass);
```

### select an element by id
```javascript
const elementById = document.getElementById("myElement");
console.log(elementById);
```

### select elements by their tag name
```javascript
const elementsByTag = document.getElementsByTagName('p');
console.log(elementsByTag);
```

### example  (Making an arrray for a group of list items)
```javascript
const tags = document.getElementsByTagName('li');
Array.from(tags).forEach(() => {
    console.log(this.innerHTML);
});
```
---

### create a new element
```javascript
const newElement = document.createElement('p');
newElement.innerHTML = "This is a new paragraph.";
document.body.appendChild(newElement);
```
---

### remove an element
```javascript
const elementToRemove = document.getElementById("myElementToRemove");
document.body.removeChild(elementToRemove);
```
---

### change an attribute of an element
```javascript
document.querySelector('img').src = "newImage.jpg";
```
---

## DOM Navigation

### first element child
```javascript
console.log(document.querySelector('body').firstElementChild);
```
### last element child
```javascript
console.log(document.querySelector('body').lastElementChild);
```
### parent element
```javascript
console.log(document.querySelector('body').parentElement);
```
### child elements
```javascript
console.log(document.querySelector('body').children);
```
### previous sibling
```javascript
console.log(document.querySelector('body').previousSibling);
```
### next sibling
```javascript
console.log(document.querySelector('body').nextSibling);
```
### previous element sibling
```javascript
console.log(document.querySelector('body').previousElementSibling);
```
### next element sibling
```javascript
console.log(document.querySelector('body').nextElementSibling);
```
### child nodes
```javascript
console.log(document.querySelector('body').childNodes);
```
### first child
```javascript
console.log(document.querySelector('body').firstChild);
```
### last child
```javascript
console.log(document.querySelector('body').lastChild);
```
### parent node
```javascript
console.log(document.querySelector('body').parentNode);
```
### node type
```javascript
console.log(document.querySelector('body').nodeType);
```
### node value
```javascript
console.log(document.querySelector('body').nodeValue);
```
### text content
```javascript
console.log(document.querySelector('body').textContent);
```
### inner text
```javascript
console.log(document.querySelector('body').innerText);
```
### inner HTML
```javascript
console.log(document.querySelector('body').innerHTML);
```
---

## Event listeners


### click event
```javascript
document.querySelector('button').addEventListener('click', function() {
    console.log('Button clicked');
});
``` 

---

### keydown event
```javascript
document.addEventListener('keydown', function(event) {
    if (event.key === 'Enter') {
        console.log('Enter key pressed');
    }
});
```
---

### keyup event
```javascript
document.addEventListener('keyup', function(event) {
    console.log(`Key = ${event.key}`);
});
```
---

### mouseover event
```javascript
document.querySelector('button').addEventListener('mouseover', function() {
    console.log('Mouse over button');
});
```
---

### mouseout event
```javascript
document.querySelector('button').addEventListener('mouseout', function() {
    console.log('Mouse out of button');
});
```
---

### mouseenter event
```javascript
document.querySelector('button').addEventListener('mouseenter', function() {
    console.log('Mouse entered button');
});
```
---

### mouseleave event
```javascript
document.querySelector('button').addEventListener('mouseleave', function() {
    console.log('Mouse left button');
});
```
---

### focus event
```javascript
document.querySelector('input').addEventListener('focus', function() {
    console.log('Input field focused');
});
```
---

### blur event
```javascript
document.querySelector('input').addEventListener('blur', function() {
    console.log('Input field blurred');
});
```
---

### input event
```javascript
document.querySelector('input').addEventListener('input', function() {
    console.log('Input field value changed');
});
```
---

### change event
```javascript
document.querySelector('input').addEventListener('change', function() {
    console.log('Input field value changed');
});
```
---

### submit event
```javascript
document.querySelector('form').addEventListener('submit', function(event) {
    event.preventDefault(); ### prevent form from submitting
    console.log('Form submitted');
});
```
---

### animation event
```javascript
document.querySelector('button').addEventListener('animationend', function() {
    console.log('Animation ended');
});
```
---

### transitionend event
```javascript
document.querySelector('button').addEventListener('transitionend', function() {
    console.log('Transition ended');
});
```
---

### error event
```javascript
document.querySelector('button').addEventListener('error', function(event) {
    console.log('An error occurred:', event.error);
});
```
---

### remove event listener 
```javascript
const eventListener = () => {
    console.log('Button clicked');
};

document.querySelector('button').addEventListener('click', eventListener);

document.querySelector('button').removeEventListener('click', eventListener);
```
---

## Class List

### Add a class to an existing element
```javascript
document.querySelector('button').classList.add('newClass');

### Remove a class from an existing element
```javascript
document.querySelector('button').classList.remove('newClass');
```

### Toggle a class on an existing element
```javascript
document.querySelector('button').classList.toggle('newClass');
```

### Check if an element has a specific class
```javascript
console.log(document.querySelector('button').classList.contains('newClass'));
```

###  replace a class with another one
```javascript
document.querySelector('button').classList.replace('oldClass', 'newClass');
```

---

### creating a new element
```javascript
const newElement = document.createElement('p');
```

###  set the text content of the new element
```javascript
newElement.textContent = "This is a new paragraph.";
```

###  append the new element to the body of the document
```javascript
document.body.appendChild(newElement);
```

---

## Add & Change HTML

###  append HTML
```javascript
const html = document.createElement("h1");
html.textContent = "This is a new heading";
document.querySelector('p').append(html);
```

###  prepend HTML
```javascript
const newHtml = document.createElement("p");
newHtml.textContent = "This is a new paragraph.";
document.querySelector('p').prepend(newHtml);
```

###  insert before
```javascript
const newParagraph = document.createElement("p");
newParagraph.textContent = "This is a new paragraph.";
document.querySelector('p').insertBefore('beforebegin', newParagraph);
```

###  insert after
```javascript
const newParagraphAfter = document.createElement("p");
newParagraphAfter.textContent = "This is a new paragraph after.";
document.querySelector('p').insertAfter('afterend', newParagraphAfter);
```

---
