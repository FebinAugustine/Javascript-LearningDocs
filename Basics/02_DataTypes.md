# JavaScript Zero To Hero

## 02. Basics - Data Types

We saw data or values can be stored in containers called variables. This data/values can be of different types like numbers, words, sentences, true or false, etc.

- In JS there are two categories of data types, one is primitive and non-primitive.
- Primitive data types go into Stack memory
- And non primitive go into Heap memory
- In Stack memory you will get a copy
- And in Heap memory you will get a reference

### Primitive data types:

- String

```Javascript
const userName = “john”;
```

- Number

```Javascript
const userId = 123;
```

- Bigint

```Javascript
let bigNumber = BigInt(“132456789456132456481212546548975156”);
```

- Boolean

```Javascript
let isLoggedIn = true;
```

- Undefined

```Javascript
let userEmail;
```

- Symbol

```Javascript
let myLuckyNum = Symbol(“159”);
```

- Object

```Javascript
let rollNumber = null;
```

### Non Primitive data types:

- Array

```Javascript
let myArray = [1, 2, 3];
let mySecArr = [ “Bingo”, “Jango”, “Ringo”];
```

- Object

```Javascript
Let myObj = { userName: “John”, age: 18, email: “myemail@me.com” };
```

- In Javascript we don't need to explicitly say what the datatype of a variable is.
- Use double or single quotes while declaring a variable of type string.
- Data types are dynamic. Once initialized we can change the variable type by reinitializing.

#### Example:

```Javascript
let x = 1;
x = “john”;
```

- To declare more than one value in a single variable we use arrays.
- To store multiple values in a single variable in a key value format we use objects.

## Type Conversion:

In JS you can convert one data type to another which is called type conversions. Once converted we need to store it in a new variable. below are some examples.

#### Convert number to string:

```Javascript
let x = 12;
let newX = String(x);
```

#### Convert string to number:

```javascript
let age = “22”;
let newAge = Number(age);
```

#### Convert number to boolean:

```Javascript
let isLogged = 1;
let newIsLogged = Boolean(isLogged);
// output: true
```

## Console.log:

We learned how to create or declare a variable. Now to see what we have created we can use console.log();

- Javascript needs an environment to run. Either a web browser or any run time environment like nodeJs, Deno, Bun, etc.
- In both we can use console.log(); to see something.
- If using nodeJs you can use terminal to see the output using console.log();
- If inside web browser like chrome, mozilla, brave, etc. use built in console to use console.log();

#### Example:

```Javascript
let newVar = “Hello”;
```

To see the above declared variable use:

```Javascript
console.log(newVar); // output: Hello
```

To see the data type of something we use the “typeof” keyword.

#### Example:

```Javascript
let userName = “John”;
console.log(typeof userName);
// this will show the output: string
```

## Comments:

Inside our code we can write something called comments. What we write as comments will not get run as code. To write a comment we use // or /\* \*/.

```Javascript
// This is my comment. Single line comment

/*
This is my multi line comment. What ever you write inside this will be considered as comments and will get executed as this is not a code.
*/
```
