# JavaScript Zero To Hero

## 01. Intermediate - Functional Programming Paradigm

Functional programming is a programming paradigm that emphasizes functions as the building blocks of applications. It focuses on:

- <p style="font-weight: 700">Pure Functions:</p> Functions that always return the same output for a given set of inputs and have no side effects (don't modify external state).
- <p style="font-weight: 700">Immutability:</p> Data structures are treated as immutable, meaning they cannot be changed after creation. New data structures are created to represent modifications.
- <p style="font-weight: 700">First-Class Functions:</p> Functions can be assigned to variables, passed as arguments to other functions, and returned from functions, just like any other data type.
- <p style="font-weight: 700">Higher-Order Functions:</p> Functions that operate on other functions (taking functions as arguments or returning functions).

## Core Concepts in JavaScript:

Even though JavaScript isn't purely functional, it supports many functional programming concepts:

### First-Class Functions:

JavaScript functions are first-class citizens. You can treat them like any other data type:

```Javascript
const greet = function(name) {
return "Hello, " + name;
}

const sayHello = greet; // Assigning a function to a variable
console.log(sayHello("Alice")); // Output: Hello, Alice
```

### Pure Functions:

Pure functions are desirable in functional programming. They:

- Take a set of inputs and return an output based solely on those inputs.
- Don't modify any external state (variables outside the function).
- Are predictable and easier to reason about.

```Javascript
function add(x, y) {
return x + y;
}

const result1 = add(5, 3); // result1 will be 8
const result2 = add(5, 3); // result2 will also be 8 (predictable output)
```

### Immutability:

While JavaScript allows modifying objects and arrays, functional programming encourages immutability. You create new data structures with the desired changes instead of mutating existing ones.

```Javascript
const numbers = [1, 2, 3];

// Functional approach (creating a new array)
const doubledNumbers = numbers.map(number => number \* 2);

// Imperative approach (modifying the original array)
// numbers.forEach(number => number \* 2); // This wouldn't create a new array

console.log(numbers); // Output: [1, 2, 3] (original remains unchanged)
console.log(doubledNumbers); // Output: [2, 4, 6] (new array with doubled values)
```

### Higher-Order Functions:

These functions operate on other functions. Common examples include:

- map(): Applies a function to each element in an array and returns a new array with the results.
- filter(): Creates a new array with elements that pass a test implemented by the provided function.
- reduce(): Reduces an array to a single value by applying a function against an accumulator and each element.
- forEach(): Executes a provided function once for each array element.

```Javascript
const numbers = [1, 2, 3];

const doubledNumbers = numbers.map(number => number \* 2);
const evenNumbers = numbers.filter(number => number % 2 === 0);

console.log(doubledNumbers); // Output: [2, 4, 6]
console.log(evenNumbers); // Output: [2]
```

### Benefits of Functional Programming in JavaScript:

- Immutability promotes referential transparency: Code becomes easier to reason about and test as the output depends solely on the inputs.

* Pure functions are reusable and predictable: They can be used in different contexts without unexpected side effects.

* Higher-order functions lead to concise and expressive code: They reduce boilerplate code and improve readability.

#### Things to Consider:

- Functional programming can have a steeper learning curve compared to imperative programming (focusing on state changes).
- Some optimizations might be less intuitive compared to imperative approaches.

By understanding and applying functional programming concepts in JavaScript, you can write cleaner, more maintainable, and testable code. It promotes a different way of thinking about problem-solving and can be a valuable tool in your JavaScript developer toolkit.
