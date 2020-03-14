# VARIABLES

Variable is used to label and store data in computer memory.
Variable can update information stored in variable,
reference or get information stored in a variable.

Its important to distinguish that variable are not value, they contain value and represent them.

`Let` and `const` are new keyword to declare a variable, introduced in `ES6`. Prior to that programmers can declare variable with only the `var` keyword. example:

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

If the `let` variable is declared without a value, the variable will be automatically initialized with a value of `undefined` example:

```js
let myAge;
console.log(myAge); // output: undefined.
```


The `let` keyword is similar to using the `var` keyword because, anything that can be done with `var` can be done with `let`.

The `const` keyword however cannot because its constant. If you try reassigning a `const` variable, a `TypeError`, will be thrown. example:

```js
const myCity = "Lagos";
console.log(myCity); // output: Lagos
myCity = "Ibadan";
console.log(myCity); // output: TypeError
```

If a `const` variable is not assigned any value, a `SyntaxError`would be thrown. example:

```js
const myAge;
console.log(myAge); // output: SyntaxError
```


`const` keyword should only be use if programmers are sure the value will not be reassigned in the future.

### Mathematical Assignment Operators:
This is using `math operators` and variable to calculate new variable and assign to a variable. example:

```js
let goal = 2;
goal = goal + 3;
console.log(goal); // output: 5
```

In the above example, we decleared the variable `goal` with the number `2` and assigning to it `goal = goal + 3` increased the value of `goal = 2`, to `5`.

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

- a template literal is wrapped by backticks ` (this key is usually located on the top of your keyboard, left of the 1 key).
- Inside the template literal, you’ll see a placeholder, ${myPet}. The value of myPet is inserted into the template literal.
- When we interpolate `I own a pet ${myPet}.`, the output we print is the string: 'I own a pet cat.'

### Typeof

The `typeof` operator checks the value to its right and returns, or passes back, a string of the data type.

```js
const food = 'Beans';
console.log(typeof food); // Output: string

const total = 10;
console.log(typeof total); // Output: number

const string = false; 
console.log(typeof string); // Output: boolean