# JavaScript Conditional Statements

Conditional statements is like a decision we make based on circumstances. For example if i wake up very early, i do some exercise e.g Road work and cardio, else if i wake up 30mins late, i skip road work, and do just cardio, else i eat breakfast and write some code. These if-else decisions can be modeled in code by creating conditional statements. A conditional statement checks specific condition(s) and performs a task based on the condition(s).

### `if` Statement

In programming, task can be perform based on a condition using an `if` statement. example:

```js
if (true) {
    console.log('Print this message!');
} // output: Print this message!
```
The if statement is composed by writing:

- The `if` keyword followed by a set of parentheses () which is followed by a code block, or block statement, indicated by a set of curly braces {}.
- Inside the parentheses (), a condition is provided that evaluates to true or false.
- If the condition evaluates to true, the code inside the curly braces {} runs, or executes.
- If the condition evaluates to false, the block won’t execute.

### `else` Statement

If we wanted to add some default behavior to the `if` statement, we can add an `else` statement to run block of code, when the condition evaluate to false. example:

```js
if (false) {
    console.log('The code in this block will not run');
} else {
    console.log('But the code in this block will');
} // output: But the code in this block will
```

An `else` statement must be paired with an `if` statement, and together they are referred to as an `if...else` statement.

 - `else` keyword is used following the code block of an `if` statement.
- Has a code block that is wrapped by a set of curly braces {}.
- The code inside the `else` statement code block will execute when the `if` statement’s condition evaluates to false.
`if...else` statements allow us to automate solutions to yes-or-no questions, also known as binary decisions.

### Comparison Operator

When writing conditional statement, we sometimes need to use different types of operator to compare values. these operators are called comparison operators.
#### List of some comparison operators and their syntax

- less than `<`
- greater than `>`
- less than or equal to `<=`
- greater than or equal to `>=`
- equal to `===`
- not equal to `!==`

Comparison operators compare the value on the left with the value on the right. Example:

```js
10 < 12 // Evaluate to true
```

We can also use comparison operators on different data types like strings:

```js
'apples' === 'oranges' // false
```
 Since the two strings are not the same, the comparison statement evaluates to false. All comparison statements evaluate to either true or false and are made up of:

- Two values that will be compared.
- An operator that separates the values and compares them accordingly (>, <, <=,>=,===,!==).
Example:

```js
let hungerLevel = 7;
if (hungerLevel >= 7) {
  console.log('Time to eat!');
} else {
  console.log('We can eat later!');
}// output = Time to eat!
```

Note: There are difference between `===` and `==` and also `!==` and `!=`. If the two operands
 are of the same type and have the same value, then `===` produces true and `!==` produces false. The `==` and `!=` do the right thing when the operands
 are of the same type, but if they are of different types, they attempt to coerce the values. examples:

 ```js
 17 == '17'   // true
 17 === '17'   // false

false == '0'  // true
false === '0'  // false

'string' == 'string' // true
'string' === 'string' // true
 ```

 it's best practice to use the `===` and `!==` operators, unless you fully understand the conversions that take place with `==` and `!=`.


### Logical operators

In conditionals, boolean `true` or `false` values will most times be in use. In javaScript *logical operators* is use to work with boolean value. There are three(3) logical operators:

- The `and` operator (`&&`)
- The `or` operator (`||`)
- The `not` (`!`)

When we use the `&&` operator, we are checking that two things are true:

```js
if (stopLight === 'green' && pedestrians === 0) {
  console.log('Go!');
} else {
  console.log('Stop');
}
```

When using the `&&` operator, both conditions must evaluate to true for the entire condition to evaluate to true and execute. Otherwise, `if` either condition is false, the `&&` condition will evaluate to false and the `else` block will execute.
If we only care about either condition being true, we can use the `||` operator:

```js
if (day === 'Saturday' || day === 'Sunday') {
  console.log('Enjoy the weekend!');
} else {
  console.log('Do some work.');
}
```

When using the `||` operator, only one of the conditions must evaluate to true for the overall statement to evaluate to true.

The `! not` operator reverses, or negates, the value of a boolean:

```js
let excited = true;
console.log(!excited); // Prints false

let sleepy = false;
console.log(!sleepy); // Prints true
```
Essentially, the ! operator will either take a true value and pass back false, or it will take a false value and pass back true.

Logical operators are often used in conditional statements to add another layer of logic to our code.

### Truthy and Falsy

`truthy` an `falsy` are used to evaluate a non-boolean condition, like string and numbers.

Here’s an example:

```js
let myVariable = 'I Exist!';
if (myVariable) {
   console.log(myVariable)
} else {
   console.log('The variable does not exist.')
}
```

The code block in the if statement will run because myVariable has a truthy value; even though the value of myVariable is not explicitly the value true, when used in a boolean or conditional context, it evaluates to true because it has been assigned a non-falsy value.

Falsy values are:
- 0
- Empty strings like `""` or `''`
- `null` which represent when there is no value at all
- `undefined` which represent when a declared variable lacks a value
- `NaN` which means *Not a Number*

Here’s an example with numbers:

```js
let numberOfApples = 0;

if (numberOfApples){
   console.log('Let us eat apples!');
} else {
   console.log('No apples left!');
} // Prints 'No apples left!'
```

The condition evaluates to false because the value of the numberOfApples is 0. Since 0 is a falsy value, the code block in the else statement will run.


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

Like if...else statements, ternary operators can be used for conditions which evaluate to true or false.


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

`if/else if/else` statements are read from top to bottom, so the first condition that evaluates to true from the top to bottom is the block that gets executed.

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
```
- The switch keyword initiates the statement and is followed by ( ... ), which contains the value that each case will compare. In the example, the value or expression of the switch statement is stopLight.
- Inside the block, { ... }, there are multiple cases. The case keyword checks if the expression matches the specified value that comes after it. The value following the first case is `'red'`. If the value of stopLight equalled `'red'`, that case‘s console.log() would run.
- The value of stopLight is `'yellow'`, so the second case runs— `'Slow down'` is logged to the console.
- The `break` keyword tells the computer to exit the block and not execute any more code or check any other cases inside the code block. Note: Without the `break` keyword at the end of each case, the program would execute the code for all matching cases and the default code as well. This behavior is different from `if/else` conditional statements which execute only one block of code.
- At the end of each switch statement, there is a default statement. If none of the cases are true, then the code in the default statement will run.

#### Let use conditional statement to provide solution to some javaScript problems.

##### Task
Complete the getGrade(score) function, It has one parameter: an integer,**score** , denoting the number of points Julia earned on an exam. It must return the letter corresponding to her **grade** according to the following rules:

- if 25 < score <= 30 then *grade* = **A**
- if 20 < score < 25 then *grade* = **B**
- if 15 < score < 20 then *grade* = **C**
- if 10 < score < 15 then *grade* = **D**
- if 5 < score < 10 then *grade* = **E**
- if 0 <= score < 5 then *grade* = **F**

**Solution**

```js
function getGrade(score) {
    let grade;
    if (0 <= score && score <= 5) {
        grade = "F";
    } else if (5 < score && score <= 10) {
        grade = "E";
    } else if (10 < score && score <= 15) {
        grade = "D";
    } else if (15 < score && score <= 20) {
        grade = "C";
    } else if (20 < score && score <= 25) {
        grade = "B";
    } else if (25 < score && score <= 30) {
        grade = "A";
    } else {
      grade = "Did not take test!"
    }
    return grade;
}
console.log(getGrade(11));
// output : D.
``` 

Good, now that we've seen the `if...else` and `else if` in action, let see how the `switch` statement works. 

##### Task
Complete the getLetter(s) function in the editor. It has one parameter: a string, *s*, consisting of lowercase English alphabetic letters (i.e., a through z). It must return A, B, C, or D depending on the following criteria:
- If the first character in string *s* is in the set {a, e, i, o, u}, then return A.
- If the first character in string *s* is in the set {b, c, d, f, g}, then return B.
- If the first character in string *s* is in the set {h, j, k, l, m}, then return C.
- If the first character in string *s* is in the set {n, p, q, r, s, t, v, w, x, y, z}, then return D.

**Solution**

```js
function getLetter(s) {
    let letter;
   switch (s.charAt(0)) {
        case("a"):
        case("e"):
        case("i"):
        case("o"):
        case("u"):
            letter = "A";
            break;
        case("b"):
        case("c"):
        case("d"):
        case("f"):
        case("g"):
            letter = "B";
            break;
        case("h"):
        case("j"):
        case("k"):
        case("l"):
        case("m"):
            letter = "C";
            break;
        default:
            letter = "D";
            break;
    }
    return letter;
}
console.log(getLetter("adfgt"));
// output : A
```
That is how coditional statements are use to solve problems.


### Resources

- [MDN (mozilla developers network)](https://developer.mozilla.org/en-US/)
- [Codecademy](codecademy.com)
- [W3schools](w3schools.com)
- [Hackerrank (coding challange)](https://www.hackerrank.com/domains/tutorials/10-days-of-javascript).