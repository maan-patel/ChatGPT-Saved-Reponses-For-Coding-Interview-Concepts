# Q: Can you explain the concept of prototypal inheritance in Javascript?

## A: Prototypal inheritance is a way of creating new objects in Javascript that inherit properties and methods from their parent objects. In prototypal inheritance, an object's prototype can be used to create new objects that inherit from it.

Here is an example of prototypal inheritance in Javascript:

```javascript
let animal = {
  eats: true,
  walk() {
    console.log("Animal is walking");
  }
};
```

let rabbit = Object.create(animal);
rabbit.jump = function() {
  console.log("Rabbit is jumping");
};

console.log(rabbit.eats); // Output: true
rabbit.walk(); // Output: "Animal is walking"
rabbit.jump(); // Output: "Rabbit is jumping"
In this example, the rabbit object inherits the eats property and the walk method from the animal object. It also has its own jump method.

# Q: Can you explain the concept of async/await in Javascript?

## A: Async/await is a syntax for handling asynchronous code in Javascript. Asynchronous code is code that is executed in a non-blocking way, allowing other code to run concurrently. Async/await makes it easier to write and read asynchronous code by allowing you to use synchronous-style code blocks.

Here is an example of using async/await in Javascript:

```javascript
async function getData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

getData();
```
In this example, the getData function is an async function that makes an API call to retrieve some data. The fetch function returns a promise, which is a special object that represents the result of an async operation. The await keyword is used to pause the execution of the function until the promise is resolved. If the promise is rejected, the error is caught in the catch block.

# Q: Can you explain the concept of higher-order functions in Javascript?

## A: Higher-order functions are functions that take other functions as arguments or return functions as output. Higher-order functions are a key feature of functional programming, which is a programming paradigm that emphasizes the use of functions to solve problems.

Here is an example of a higher-order function in Javascript:

```javascript
function add(x) {
  return function(y) {
    return x + y;
  }
}

const addTwo = add(2);
console.log(addTwo(3)); // Output: 5
console.log(addTwo(4)); // Output: 6
```
In this example, the add function is a higher-order function that takes a number x and returns a function that takes a number y and returns the sum of x and y. The addTwo function is a closure that captures the value of x as 2. When the addTwo function is called with different values of y, it returns the sum of `