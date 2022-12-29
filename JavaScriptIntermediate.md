# 1. What is the difference between == and ===?
== is a comparison operator that performs type coercion, meaning it converts the operands to the same type before making the comparison. === is a strict comparison operator that does not perform type coercion, meaning it compares the operands without converting them to a common type.

For example:

```javascript
console.log(1 == '1'); // Output: true
console.log(1 === '1'); // Output: false
```
# 2. Can you explain the difference between synchronous and asynchronous code in JavaScript?
Synchronous code is executed in a linear, blocking manner. This means that the code is executed in the order that it appears and the next line of code will not be executed until the current line has completed.

Asynchronous code, on the other hand, is executed in a non-blocking manner. This means that the code is executed in the background and does not block the main thread of execution. Asynchronous code is typically used when dealing with I/O operations, such as making HTTP requests or reading from a file.

# 3. What is a closure in JavaScript, and how/when is it used?
A closure is a function that has access to the variables in its outer (enclosing) function’s scope, even after the outer function has returned. This is because the inner function retains a reference to the outer function’s variables.

Closures are commonly used in JavaScript for creating private variables and methods, as well as creating function factories.

Here is an example of a closure in action:

```javascript
function outerFunction(x) {
  let y = x;
  return function innerFunction() {
    console.log(y);
  }
}

let myClosure = outerFunction(5);
myClosure(); // Output: 5
```
# 4. Can you explain the concept of "hoisting" in JavaScript?
In JavaScript, variables and function declarations are "hoisted" to the top of their scope. This means that they are available to be used throughout their scope, even before they are declared.

For example:

```javascript
console.log(x); // Output: undefined
var x = 5;
Even though the x variable is declared after the console.log statement, it is still accessible because it is hoisted to the top of its scope.

Function declarations are also hoisted, but function expressions are not. This means that you can call a function before it is declared, as long as it is declared using a function declaration:

```javascript
foo(); // Output: "Hello, world!"

function foo() {
  console.log("Hello, world!");
}
```
# 5. Can you explain the difference between a "primitive" data type and an "object" data type in JavaScript?
In JavaScript, there are two main types of data: primitive data types and object data types.

Primitive data types include numbers, strings, booleans, null, and undefined. These data types are immutable, meaning they cannot be changed or modified.

Object data types include arrays, functions, and objects. These data types are mutable, meaning they can be changed and modified.

Here is an example of a primitive data type (a number) and an object data type (an array):