## Function
A function is a reuseable block of code, that group together a sequence of statement to peform a specific task.
### Function declaration
in javaScript they are many ways to declare a function.One way to create a function is by using a `function` declaration. example:

```js
function teamNames() {
    console.log('Liverpool', 'Barcelona');
}
console.log(teamNames()); // Liverpool, Barcelona
```
### Calling a function
A function is called when `function` name followed by the parentheses is typed. From the example above

```js
console.log(teamNames());
```
called the function inside `teamNames`.

### Parameter and Argument
parameter allows function accept input(s), and perform a task using the input(s). When declaring a function we can specify a parameter. example:

```js
function aggregateScore(Home, Away) {
    console.log(Home + Away);
}
```
the value passed to the functiion when they are called, are called `argument`. it can be passed as a value or variable example:

```js
function aggregateScore(Home, Away) {
    console.log(Home + Away);
}
aggregateScore(4 + 2)// 6
```

### Default parameters
in `ES6` default parameter feature is included, with the ability to have a predetermined value, in case  there is no argument passed into function or the argument is undefined when called. example:

```js
please it will be in the full article
```
### Return
when a function is called, the computer will run through the functions code and evaluate the result of calling the function. thee `return` keyword allow us see the calculation that the computer did print example:

```js 
function totalNumber(cash, bank) {
    return 30 +80;
}
console.log(totalNumber()); // 11
```

### Function Expression
 Another way of defining a function is to use a function expression. example:
 
 ```js
 const myName = Function(boy {

 })
  ```

  ### Arrow Function
  arrow function is another way to deefine function introduced by the `ES6` It's a shorter way to write function using the `=>` arrow. example:

  ```js
  const plantNeedWater = (day) => {
      if (day === 'Monday') {
          return true;
      }
  }
```

To discuss more on function in the full article.

