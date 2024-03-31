# JavaScript Zero To Hero

## 01. Intermediate - Asynchronous Programming

- Javascript is a synchronous programming language. One by one execution.
- Runs on single thread.

## Execution Context:

Each line of code waits for the above to be executed.

## Blocking code and Non blocking code.

- Blocking code blocks the entire code flow. This means synchronous.
- Non blocking means it does not block the flow of the entire code. This means asynchronous.
- async/await is a powerful mechanism in JavaScript for handling asynchronous operations in a more synchronous-like manner.

## Understanding Asynchronous Operations

JavaScript is single-threaded, meaning it can only execute one task at a time. However, many web applications involve asynchronous operations like fetching data from servers or waiting for user input. These operations don't block the main thread, allowing other parts of your code to run while waiting for the asynchronous task to complete.

## Challenges of Callbacks and Promises

Traditionally, asynchronous operations were handled using callbacks or promises. These approaches can lead to nested callbacks (callback hell) or complex promise chains, making code difficult to read and maintain.
