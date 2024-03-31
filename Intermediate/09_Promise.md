# JavaScript Zero To Hero

## 01. Intermediate - Promise

- Promises are a fundamental concept in JavaScript for handling asynchronous operations
- Before promises, callbacks were the primary way to handle asynchronous operations.
- This approach can lead to nested callbacks, creating what's known as "callback hell," making code difficult to read, maintain, and debug.
- Promises offer a more structured way to handle asynchronous operations.
- A promise is an object that represents the eventual completion (or failure) of an asynchronous operation.

### It has three states:

- Pending: The initial state, indicating the operation is ongoing.
- Fulfilled: The operation completed successfully, and the promise holds the resolved value.
  Rejected: The operation failed, and the promise holds the reason for the failure.

## Creating promise using constructor and consuming it:

#### Example 1:

```Javascript
const promise = new Promise((resolve, reject) => {
setTimeout(function () {
console.log(“Async function here.”);
resolve()
}, 1000)
});

promise.then(function(){
console.log(“then resolved”);
}).catch( error ){
console.log( error );
}
```

#### Example 2:

```Javascript
const promise = new Promise((resolve, reject) => {
setTimeout(function () {
let myObj = { user: “John” }
resolve( myObj )
}, 1000)
});

promise.then(function( myObj ){
console.log(myObj);
}).catch( error ){
console.log( error );
}
```

#### Example 3:

```Javascript
const promise = new Promise((resolve, reject) => {
setTimeout(function () {
let error = true;
if(!true) {
let myObj = { user: “John” }
resolve( myObj )
} else {
reject(“Error: error”)
}
}, 2000)
});

promise.then(function( myObj ){
console.log(myObj);
}).catch( error ){
console.log( error );
}
```

#### Example 4:

```Javascript
const promise = new Promise((resolve, reject) => {
    setTimeout(function () {
    let error = true;
    if(!true) {
    let myObj = { user: “John” }

        resolve( myObj )
        } else {
        reject(“Error: error”)
        }
    }, 2000)
});

promise.then(function( myObj ){
return myObj.user
})
.then(function( user){
console.log( user );
})
.catch( ( error )=>{
console.log( error );
})
.finally(()=> “Finally this will run”)
```

## Promise with Async

```Javascript
const promise = new Promise((resolve, reject) => {
    setTimeout(function () {
        let error = true;
    if(!true) {
        let myObj = { user: “John” }
        resolve( myObj )
        } else {
        reject(“Error: error”)
        }
    }, 2000)
});
async function consumePromise() {
	try {
		const response = await promise;
		console.log( response );
}catch(err) {
	console.log(“Error:”, err);
}
}
consumePromise()
```
