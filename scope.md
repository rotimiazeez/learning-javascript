## Scope
They are two scope used in javaScript.

### Globe scope
In globe scope variables are define outside of blocks. these variables are call globe variable. Because globe variables are not bound in a blocl, they can be accessed by any code in the program, including codes in block. example:

```js
const color = 'blue';
const returnSkyColor = () => {
    return color;
}
console.log (returnSkyColor();)
```

### Block scope
When a variable is define in a block, it is only accessible to the code within the curly braces {}. Variables declared within the block scope are called local variables. example:

```js
const logSkyColor = () => {
    let color = 'blue';
    console.log(color);// blue
}
logSkyColor(); // blue
console.log(color); // Reference Error

```

I will explain `scope pollution`, and `scope best practice` in the full articule.