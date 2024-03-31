# JavaScript Zero To Hero

## 01. Intermediate - Async Await

Async/await syntax simplifies asynchronous code by introducing two keywords:

- async: This keyword is placed before a function declaration to mark it as asynchronous. An async function can contain an await expression.
- await: This keyword is used within an async function to pause its execution until a promise is settled (resolved or rejected). The await expression is then replaced with the fulfilled value of the promise.

#### Example:

```Javascript
async function fetchData() {
  const response = await fetch('https://api.example.com/data');
  const data = await response.json();
  return data;
}

fetchData()
  .then(data => {
   	 console.log(data);
  })
  .catch(error => {
   	 console.error(error);
  });
```

## try… catch…

It's better to use try catch inside async function also.
Multiple .then can be used.

```Javascript
async function fetchData() {
try {
const response = await fetch('https://api.example.com/data');
const data = await response.json();
return data;
}catch(error) {
console.log(“Error: ”, error);
}
}

fetchData()
.then(data => {
console.log(data);
})
.catch(error => {
console.error(error);
});
```
