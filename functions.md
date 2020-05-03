## Function

A function is a reusable block of code, that group together a sequence of statements to perform a specific task.

### Function declaration

In javaScript they are many ways to declare a function.One way to create a function is by using a `function` declaration. example:

```js
function teamNames() {
  console.log("Liverpool", "Barcelona");
}
console.log(teamNames()); // Liverpool, Barcelona
```

A function declaration consists of:

- The function keyword.
- The name of the function, or its identifier, followed by parentheses.
- A function body, or the block of statements required to perform a specific task, enclosed in the function’s curly brackets, { }.

### Calling a function

A function is called when `function` name followed by the parentheses is typed. From the example above

```js
console.log(teamNames());
```

called the function inside `teamNames`.

### Parameter and Argument

The Parameter allows function accepts input(s), and perform a task using the input(s). When declaring a function we can specify a parameter. We use parameters as placeholders for information that will be passed to the function when it is called. example:

```js
function aggregateScore(home, away) {
  console.log(home + away);
}
```

the value passed to the functiion when they are called, are called `argument`. it can be passed as a value or variable example:

```js
function aggregateScore(Home, Away) {
  console.log(Home + Away);
}
aggregateScore(4 + 2); // 6
```

### Default parameters

in `ES6` default parameter feature is included, with the ability to have a predetermined value, in case there is no argument passed into function or the argument is `undefined` when called. example:

```js
function greeting(name = "stranger") {
  console.log(`Hello, ${name}!`);
}

greeting("Nick"); // Output: Hello, Nick!
greeting(); // Output: Hello, stranger!
```

By using a default parameter, we account for situations when an argument isn’t passed into a function that is expecting an argument.

### Return

When a function is called, the computer will run through the functions code and evaluate the result of calling the function. By default that resulting value is undefined. example:

```js
function monitorCount(rows, columns) {
  let total = rows + columns;
}
console.log(monitorCount(3 + 5)); // print undefined
```

the `return` keyword allow us see the calculation that the computer did print example:

```js
function totalNumber(cash, bank) {
  return 30 + 80;
}
console.log(totalNumber()); // 11
```

The `return` keyword is powerful because it allows functions to produce an output. We can then save the output to a variable for later use

### Function Expression

Another way of defining a function is to use a function expression. example:

```js
const myName = Function(boy) {

};
```

To declare a function expression:

- Declare a variable to make the variable’s name be the name, or identifier, of your function. Since the release of ES6, it is common practice to use const as the keyword to declare the variable.

- Assign as that variable’s value an anonymous function created by using the function keyword followed by a set of parentheses with possible parameters. Then a set of curly braces that contain the function body. Unlike function declarations, function expressions are not hoisted so they cannot be called before they are defined.

  ### Arrow Function

  Arrow function is another way to define function introduced by the `ES6` It's a shorter way to write function using the `=>` arrow. example:

  ```js
  const plantNeedWater = (day) => {
    if (day === "Monday") {
      return true;
    }
  };
  ```

It’s important to be familiar with the multiple ways of writing functions because you will come across each of these when reading other JavaScript code.

### Concise Body Arrow Functions

JavaScript also provides several ways to refactor arrow function syntax. The most condensed form of the function is known as the concise body.

- Functions that take only a single parameter do not need that parameter to be enclosed in parentheses. However, if a function takes zero or multiple parameters, parentheses are required.

- showcasing how arrow functions parameters differ for different amounts of parameters
  A function body composed of a single-line block does not need curly braces. Without the curly braces, whatever that line evaluates will be automatically returned. The contents of the block should immediately follow the arrow => and the return keyword can be removed. This is referred to as an implicit return.

So if we have a function:

```js
const squareNum = (num) => {
  return num * num;
};
```

We can refactor the function to:

```js
const squareNum = (num) => num * num;
```

Notice the following changes:

- The parentheses around num have been removed, since it has a single parameter.
- The curly braces { } have been removed since the function consists of a single-line block.
- The return keyword has been removed since the function consists of a single-line block.

A typical example of function and it's implementation.

```js
let factorial = (n) => {
  let num = 1;
  /*
   for (let i = 2; i <= n; i++) {
    num = num * i
   }
   */
  let i = 2;
  while (i <= n) {
    num *= i;
    i++;
  }

  return num;
};
```

### Resources

- [MDN (mozilla developers network)](https://developer.mozilla.org/en-US/)
- [Codecademy](codecademy.com)
- [W3schools](w3schools.com)
- [Hackerrank (coding challange)](https://www.hackerrank.com/domains/tutorials/10-days-of-javascript)
