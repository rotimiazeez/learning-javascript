## ARRAYS
Arrays are  javaScript ways of making list. Arrays can store any data type (including string, number, boolean). Like list, arrats are ordered, meaning each item has a numbered position. example:

```js
let newYearResolution = ['Keep ajournal', 'Take coding classes' 'Learn a craft'];
console.log(newYearResolution);
```

an array literals create an array by wrapping it in square brackets.

### Accessing Element
Each element in an array has a numbered position known as index. The index is used to access individual items. JavaScript arrays are 0 indexed, meaning the position start counting from 0 rather than 1. Example:

```js
const groceryItems = ['Toilet papers', 'Hand wash', 'Fruit'];
const items = (grocery[0]);
console.log(items); // Toilet paper.
console.log(groceryItems[2]);// Fruits.
console.log(groceryItems[3]); // undefined
```
if an ivalid index number is passed, the value undefined is returned.

### Updating Element
Array elements can be updated by accessing the item by it index number and passing it a new value. example:

```js
let season = ['Winter', 'Summer', 'Spring', 'Fall'];
season[3] = 'Autumn';
console.log(season); // ['Winter', 'Summer', 'Spring', 'Autumn'];
```
notice Fall was updated to Autumn.

### Arrays with `let` and `const`
Recall variables declared with `let` can be reassigned, and variable with `const` can not be reassigned. However element in an array decleared with `const` are mutable, meaning that we can change the content of a `const` of a const array, but cannot reassign new value. example:

```js
let condiments =['ketchup', 'Mustard', 'Soysause', 'Sriach'];
condiments [0] = ['Mayo'];
console.log(condiments);// ['Mayo', 'Mustard', 'Soysause', 'Sriach']
```
for `const`

```js
const utensils = ['Fork', 'Knife', 'Chopstick', 'Spork'];
utensils[3] = 'spoon';
console.log(utensils);// ['Fork', 'Knife', 'Chopstick', 'Spoon']

utensils = ['Knife', 'Fork'];
console.log(utensils); // TypeError
```

#### To be added to this draft

- The .length property
- Array methods ...