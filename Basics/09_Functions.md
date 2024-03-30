# JavaScript Zero To Hero

## 09. Basics - Functions

Functions are methods or blocks of code once defined you can use it anywhere anytime with just a call.

Creating a named function:

```Javascript
	function myFunction() {
		console.log(“My First Function.”);
}
```

Calling a function:

```Javascript
myFunction();
// You can call this kind of function from anywhere
```

Creating a unnamed function:

```Javascript
	let myFun = function () {
		console.log(“My First unnamed Function.”);
}
```

Calling a unnamed function:

```Javascript
myFun();
// This kind of function can be called only after its declaration line.
```

Creating a function with Parameters:

```Javascript
	function myFunction(num1, num2) {
		console.log(`First number is ${num1} and second number is ${num2}`);
}
```

Calling a function and passing arguments:

```Javascript
myFunction(3, 5);
```

Creating a function with Parameters and return:

```Javascript
	function myFunction(num1, num2) {
		console.log(`First number is ${num1} and second number is ${num2}`);
		return num1 + num 2;
}
```

Calling a function that has a return and storing it in a variable:

```Javascript
let myReturn = myFunction(3, 5);
```

### Arrow Function

#### Basic syntax:

```Javascript
() => {}
```

- Here we do not write the keyword “function” while creating.
- Shortest way of writing a function

#### Arrow function with curly braces:

```Javascript
let myArrFun = (num1, num2) => { console.log(num1); }

let myArrFun = (num1, num2) => { console.log(num1); return num2 }
```

In the arrow function if you are using curly braces and if you have a return then you should use return just like normal function.

#### Arrow function with normal braces:

```Javascript
let myArrFun = (num1, num2) => ( console.log(num1); return num2; )
```

In the arrow function if you are using normal braces and if you have a return then you don't use return keyword.

#### Implicit Arrow function:

```Javascript
let myImpArr = (num1, num2) => num1 + num2;
```

In the implicit arrow function you don't use the return keyword.

### IIFE Function

#### Immediately Invoked Function Expression:

- We know we need to call a function after it is created to work/run. But IIFE is a self working function.
- Use iife to escape global scope pollution.

#### Normal IIFE:

```Javascript
Function myIife(a, b) { console.log(a); }
```

Cover the above function in a normal brace then add another empty brace.

```Javascript
( Function myIife(a, b) { console.log(a); } )();
```

Arrow function IIFE:

```Javascript
( (a, b)=> { console.log(a); } )();
```

### Callback Function

Function passed as an argument is called a callback function.

```Javascript
function callBack(str, cbFunction) {
	console.log(`My name is ${str}`);
	cbFunction();
};
Function callBackFun() {
	console.log(`I am a call back function`);
};

callBack(“John”, callBackFun);
```

You can use arrow function also as a callback function.

```Javascript
function callBack(()=> {} ) {};
```

### High Order Function

Any function that has a function as a parameter or a function that returns a function is called a high order function.

```Javascript
function callBack( function callBackFun() {} ) {
	Return function returnFun() {
		console.log(“Return function”);
}
};
```

### Scope and Execution Context

- Curly braces { } used with function or if else or loops are called scopes in JS.
- Two types of scopes: Global and Block
- Child scope can access parent scope variables.
- But parent scope cannot access children.
- Variables declared using var keyword can be accessed from anywhere because it is considered global.
- Avoid using var instead use let and const because they are part of block scope.

### Javascript Execution Context.

#### How the flow works.

First below context get created

- Global Execution Context
- Functional Execution Context
- Evaluation Execution context

#### Memory Allocation Phase:

- allocate memory for declared variables.

#### Execution Phase:

- function gets executed.

#### Call stack:

- First in first out
