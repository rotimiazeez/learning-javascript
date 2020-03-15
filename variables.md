# VARIABLES IN JAVASCRIPT

Variable is used to label and store data in computer memory.
Variable can update information stored in variable, git reference or get information stored in a variable.
It's important to distinguish that variable is not a value, they contain value and represent them.

`let` and `const` are new keyword to declare a variable, introduced in `ES6`. Before that programmers can declare a variable with only the `var` keyword. example:

```js
var food = 'pizza';
console.log(food); // output: pizza
```

`let` keyword signal that values can be reassigned a different value e.g

```js
let myName = 'Azeez';
console.log(myName); //output: Azeez
myName = 'Rotimi';
console.log(myName); //output: Rotimi
```

`var` also can be reassigned in the same way.

`var` and `let` are both used for variable declaration in javascript but the difference between them is that `var` is function scoped and `let` is block scoped. example:

```js
console.log(x);
var x=5;
console.log(x); //Output: undefined, 5
```

if an undeclared variable is logged to the console and later declared with `var` and assigned a value, it will return undefine and the value assigned to it.

 an error will be returned if `let` is used in declaring such variable. example:

 ```js
console.log(x); // output: ReferenceError: x is not defined
let x=5;
console.log(x); //Output: 5
 ```

If the `let` variable is declared without a value, the variable will be automatically initialized with a value of `undefined` example:

```js
let myAge;
console.log(myAge); // output: undefined.
```

The `const` keyword however cannot because its constant. If you try reassigning a `const` variable, a `TypeError`, will be thrown. example:

```js
const myCity = "Lagos";
console.log(myCity); // output: Lagos
myCity = "Ibadan";
console.log(myCity); // output: TypeError
```

If a `const` variable is not assigned any value, a `SyntaxError`would be thrown. example:

```js
const myAge; // output: SyntaxError
```


`const` keyword should only be used if programmers are sure it won't be reassigned or redeclared in the future.

### Mathematical Assignment Operators:
This is using `math operators` and variable to calculate new variable and assign to a variable. example:

```js
let goal = 2;
goal = goal + 3;
console.log(goal); // output: 5
```

In the above example, we declared the variable `goal` with the number `2` and assigning to it `goal = goal + 3` increased the value of `goal = 2`, to `5`.

`goal` can be reassigned by using built-in mathematical assignment operator. example:

```js
let goal = 2;
goal += 3;
console.log(goal); // output: 5
```

> same can be done for other math operator ` -, *, /, %`

### The Increment and Decrement Operators.
Increment operator `++` and Decrement operator `--` are other mathematical assignment operators.

The Increment `++` increase the value by 1. example:

```js
let goal = 2;
goal ++;
console.log(goal); // output: 3
```

The Decrement `++` decrease the value by 1. example:

```js
let goal = 2;
goal --;
console.log(goal); // output: 1
```

### String Concatenation with Variable
The `+` operator can used to combine two string values even if those value are being stored in variable. example:

```js
let song = 'indigo';
console.log('I love ' + song + '.'); // I love indigo.
```

### String Interpolation
With `E6` we can insert, or interpolate, variable into string using template. example:

```js
const myPet = 'cat';
console.log(`I own a pet ${myPet}.`);
// Output: I own a pet cat.
```

- A template literal is wrapped by backticks (&#96;).
- Inside the template literal, you’ll see a placeholder, ${myPet}. The value of myPet is inserted into the template literal.
- When we interpolate `I own a pet ${myPet}.`, the output will print is the string: 'I own a pet cat.'

### Typeof

The `typeof` operator checks the value to its right and returns or passes back, a string of the data type.

```js
const food = 'Beans';
console.log(typeof food); // Output: string

const total = 10;
console.log(typeof total); // Output: number

const string = false; 
console.log(typeof string); // Output: boolean
```

other typeof include `undefined`, `null`, `symbol`, `object`.

### RESOURCES
 - [Codecademy] (https://www.codecademy.com/)
 - [W3schools] (https://www.w3schools.com/)
 - [MDN] (https://developer.mozilla.org/en-US/)
