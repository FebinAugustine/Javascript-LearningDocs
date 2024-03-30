# JavaScript Zero To Hero

## 10. Basics - Control Flow Statements

### if else

If( ) { } and if( ) { } else if( ) { } else{ } are used to check conditions before executing some other function or statements. Use else if you have multiple checks.

#### Using if alone

```Javascript
if (true) {
console.log("Yes i will run");
}

const isLoggedIn = true;
if (isLoggedIn) {
console.log("You are logged in..");
}

// <=, >=, !=, ==, === Conditions which you can use
// === this will strictly check the type also.
if (3 != 2) {
console.log("3 not equal to 2");
}
```

#### if else

```Javascript
const temp = 50;
if (temp < 41) {
console.log("Temperature less than 41");
} else {
console.log("Temperature greater than 41");
}
```

### Implict - one line

```Javascript
if (2 == 2) console.log("2 equal to 2");
```

### if else if else

```Javascript
if (temp < 41) {
console.log("Temperature less than 41");
} else if (temp < 50) {
console.log("Temperature less than 50");
} else {
console.log("Temperature greater than 50");
}
```

### Multiple condition checking

```Javascript
const isLoggedIn1 = false;
const paid = true;

// Check any ofthem is true
if (isLoggedIn1 || paid) {
console.log("logged in or paid");
}

// Check both are true
if (isLoggedIn1 && paid) {
console.log("Loggedin and paid");
}
```

### Switch

This is also another way of conditional checking but not like if else. Always remember to use break other wise the the code will continue till end.

```Javascript
const day = 8;
switch (day) {
  case 1:
    console.log("Sunday");
    Break;
// use break to come out of the flow
  case 2:
    console.log("Monday");
    break;
  case 3:
    console.log("Tuesday");
    break;
  case 4:
    console.log("Wednesday");
    break;

  default:
    console.log("DAY not defined");
    break;
}
```

### Ternary

This is used to check some condition and then do some thing. Just another version of if else.

#### Falsy Values

```Javascript
false, 0,-0,BigInt, 0n,"", null, undefined, NaN
```

#### Truthy Values

```Javascript
"0", "false", " ", [], {}, function(){},
```

### Ternary Operator

```Javascript
Condition ? true : false

const price = 12;
price <= 12 ? console.log("price less than 12") : console.log("price greater than 12");
```

## for Loops

### Basic for loop:

```Javascript
for (let index = 0; index = 5; index++) {
      console.log(index);
 }
// Prints the value of index until index is equal to 5
```

#### For Loop with if :

```Javascript
for (let index = 0; index <= 5; index++) {
  const element = index;
  if (element == 2) {
    console.log("2 is the number");
  }
  console.log(element);
}
```

#### For Loop with on array :

```Javascript
let arr = ["ar1", "ar2", "ar3"];
for (let index = 0; index < arr.length; index++) {
const element = arr[index];
console.log(element);
}
```

#### For Loop with if and break:

```Javascript
// Break
// comes out of the loop
for (let index = 0; index <= 5; index++) {
  const element = index;
  if (element == 3) {
    console.log("3 is the number");
    break;
  }
  console.log(element);
}
```

#### For Loop with if and continue:

```Javascript
// Continue
// skip that particular item
for (let index = 0; index <= 5; index++) {
const element = index;
if (element == 3) {
console.log("3 skipped");
continue;
}
console.log(element);
}
```

## While and do while Loops

### Basic while loop:

```Javascript
let index = 0;
while (index <= 10) {
  console.log(`The value is ${index}`);
  index = index + 2;
}
```

### Basic while loop on array:

```Javascript
let arr = ["bingo", "jango", "dingo"];
let arrr = 0;
while (arrr < arr.length) {
  console.log(`${arr[arrr]}`);
  arrr = arrr + 1;
}
```

### Basic do while loop:

```Javascript
// do while loop
// check condition after doing the job
let dos = 0;
do {
  console.log(`${dos}`);
  dos++;
} while (dos <= 5);
```

High Order Loops
For of Loops
Objects are not iterable with for of loop

const arr = [1, 2, 3, 4, 5];
for (const i of arr) {
console.log(`${i}`);
}

const char = "bingo";
for (const iterator of char) {
console.log(`${iterator}`);
}

Loop through map:
let map = new Map();
map.set("IN", "India");
map.set("FR", "France");

for (const [key, value] of map) {
console.log(key, ":", value);
}

## For in Loops

#### note: Maps are not iterable using for in loop

### Loop through objects:

```Javascript
const myObj = {
  js: "Java Script",
  cpp: "C++",
};

for (const key in myObj) {
  console.log(`${key} is shortcut for ${myObj[key]}`);
}
```

### Loop through arrays:

```Javascript
const myArr = ["b", "i", "n", "g", "o"];

for (const key in myArr) {
 	 console.log("Key is: ", key);
  	console.log("Value is: ", myArr[key]);
}
```

## For each Loops

- Used with arrays
- Is a method used to loop through each item in an array and do some job for each specified item..
- A high order function. Higher order functions are functions that take one or more functions as arguments, or return a function as their result.
- Callback function will not have a name.
- You can use the arrow function also.
- Does not return anything so you cannot assign it to a variable.

```Javascript
const myArr = ["js", "cpp", "java"];
myArr.forEach(function (item) {
console.log("items");
});
```

## for each using Arrow function

```Javascript
myArr.forEach((item) => {
console.log(item);
});
```

### for each has three parameters which you can use.

```Javascript
myArr.forEach((item, index, arr) => {
  console.log(item, index, arr);
});
```

### For each with array of objects

```Javascript
const myCoding = [
  {
    name: "Java",
    file: "Java",
  },
  {
    name: "JavaScript",
    file: "JS",
  },
  {
    name: "Python",
    file: "PY",
  },
];

myCoding.forEach((item) => {
  // console.log(item.name);
});
```

## Filter Loops

- Used with arrays
- Returns something so you can store it in a variable.
- Conditional filtering can be done.

```Javascript
const nums = [1, 2, 3, 4, 5, 6, 7];
const newNums = nums.filter((nums) => {
  	return nums > 3;
});
```

#### filter has three parameters which you can use.

```Javascript
myArr.filter((item, index, array) => {
console.log(item, index, array);
});
```

#### Filter used in an array with objects as elements.

```Javascript
const books = [
  {
    name: "bk1",
    publishDate: 1985,
    genre: "science",
  },
  {
    name: "bk2",
    publishDate: 1935,
    genre: "math",
  },
];

const userBk = books.filter((item) => item.publishDate > 1975);
console.log(userBk);
```

## Loop - map method

- Used with arrays
- Unlike filters, map returns without condition.

```Javascript
const nums1 = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let newNums1 = nums1.map((num) => {
  return num + 2;
});
console.log(newNums1);
```

### map has three parameters which you can use.

```Javascript
	Const myArr = [ 1, 2, 3, 4 ];
myArr.map((value, index, array) => {
console.log(value, index, array);
});
```

## Loop - reduce method

- Used with arrays

### reducer has three parameters which you can use.

```Javascript
	Const myArr = [ 1, 2, 3, 4 ]
	let initVal = 0;
myArr.reduce((initVal, currVal, index, array) => {
console.log(value, index, array);
}, 0 );
```

#### Example:

```Javascript
let myPrice = myArr.reduce((acc, currVal) => {
console.log(acc, currVal);
  return acc + currVal;
}, 0);

console.log(myPrice);
```
