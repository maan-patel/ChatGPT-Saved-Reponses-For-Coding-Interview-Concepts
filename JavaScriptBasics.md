# Q: What is Javascript and what is it used for?

## A: Javascript is a programming language that is primarily used for creating interactive features on websites. It is often used for tasks such as form validation, creating animations, and handling user events such as clicks and hover actions. Javascript is also used for creating mobile applications, backend applications, and games.

# Q: What is the difference between var, let, and const in Javascript?

## A: Var, let, and const are all ways to declare variables in Javascript. The main difference between them is the level of variable assignment that is allowed:

## Var: Var declarations are globally scoped or function scoped. This means that a variable declared with var can be re-assigned and updated within its scope.
## Let: Let declarations are block scoped. This means that a variable declared with let can be re-assigned and updated within its block of code, but cannot be accessed outside of that block.
## Const: Const declarations are also block scoped, but the value of a const variable cannot be reassigned. If you try to reassign a const variable, you will get a "TypeError" message.

# Q: What is the difference between null and undefined in Javascript?

## A: Null and undefined are both values that represent the absence of a value or object. However, there is a subtle difference between the two:
## Undefined: Undefined means that a variable has been declared, but it has not been assigned a value. If you try to access an undeclared variable, it will be undefined.
## Null: Null is an assignment value that represents the absence of an object. It is often used to represent the absence of a value that may be returned by a function.

# Q: Can you explain the concept of hoisting in Javascript?

## A: Hoisting is the behavior in Javascript where declarations of variables and functions are automatically moved to the top of their scope. This means that you can use a variable or function before it is declared in your code. For example:

```javascript
console.log(x); // Output: undefined
var x = 5;
```

## Even though the x variable is declared after the console.log statement, the declaration is automatically moved to the top of the code, so the value of x is undefined when it is logged. However, the value of x is not hoisted in this case, so it is still 5 when it is logged.

# Q: Can you explain the concept of closure in Javascript?

## A: A closure is a function that has access to the variables and parameters of its outer function, even after the outer function has returned. Closures are often used to create private variables and functions, and to create functions with a fixed set of parameters.

## Here is an example of a closure in Javascript:
```javascript
function outerFunction(x) {
  var y = x + 1;
  
  return function innerFunction() {
    console.log(y);
  }
}

var inner = outerFunction(5);
inner(); // Output: 6
```
## In this example, the innerFunction has access to the y variable even after the outerFunction has returned. When the innerFunction is called, it logs the value of y, which is 6.