## Simple Draft On Conditionals

### `if` Statement

In programming, task can be perform based on a condition using an `if` statement. example:

```js
if (true) {
    console.log('Print this message!');
} // output: Print this message!
```

### `else` Statement

If we wanted to add some default behavior to the `if` statement, we can add an `else` statement to run block of code, when the condition evaluate to false. example:

```js
if (false) {
    console.log('The code in this block will not run');
} else {
    console.log('But the code in this block will');
} // output: But the code in this block will
```

### Comparison Operator

When writing conditional statement, we sometimes need to use different types of operator to compare values. these operators are called comparison operators.
#### List of some comparison operators and their syntax

- less than `<`
- greater than `>`
- less than or equal to `<=`
- greater than or equal to `>=`
- equal to `===`
- not equal to `!==`

> More details will be provided on comparison operators

### Logical operators

In conditionals, boolean `true` or `false` values will most times be in use. In javaScript *logical operators* is use to work with boolean value. There are three(3) logical operators:

- The `and` operator (&&)
- The `or` operator (||)
- The `not` (!)

> Examples and more details to be provided

### Truthy and Falsy

`truthy` an `falsy` are used to evaluate a non-boolean condition, like string and numbers.
>More details to be provided.

### Ternary Operators

Ternary operators is use to simplify an `if...else` statement using short-hand syntax. example:

```js
let isNightTime = true;
if(isNightTime) {
    console.log('Turn on the light');
} else {
    console.log('Turn off the light');
}
```
This can be performed using ternary operator:

```js
let isNightTime = true;
isNightTime ?  console.log('Turn on the light') : console.log('Turn off the light');
```

### `else if` statement

`else if` statement is use to add more conditions to our `if...else` to get many possible outcome. The `else if` comes right after the `if` and before the `else` statement. example:

```js
let stopLight = 'yellow';
if (stopLight === 'red') {
    console.log('Stop!');
} else if (stopLight === 'yellow') {
    console.log('Slow down');
} else if (stopLight === 'green') {
    console.log('Go!');
}  else {
    console.log('Caution, unknown');
}
```

### Switch Keyword

A `switch` statement provide an alternative way to write the `else if` statement, with a syntax that is easier to read and write. example:

```js
let stopLight = 'yellow';
switch (stopLight) {
    case 'red' :
      console.log('Stop!');
      break;
    case 'yellow' :
       console.log('Slow down');
       break;
    case 'green' :
       console.log('Go!');
       break;
    defualt :
       console.log('Caution, unknown');
       break;
}
