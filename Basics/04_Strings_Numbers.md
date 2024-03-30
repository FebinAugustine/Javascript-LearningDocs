# JavaScript Zero To Hero

## 04. Basics - Strings & Numbers

### Single - Double - Backticks

Strings are for storing content in text format. We know how to declare a string.

```Javascript
let strDq = “Double Quote”;
```

We can use single quotes also to declare a string variable.

```Javascript
let strSq = ‘Single Quote’;
```

Another way is to use backticks. Strings enclosed in backticks are called templates.

```Javascript
let strBt = `This is a string inside backticks`
```

#### Note:

- You cannot use double quotes inside a string which uses double quotes while declaring. Likewise while using single quotes during declaration another single quote cannot be used.
- But you can use single quotes inside double quotes and vice versa.
- In contrast you can use single and double quotes if you are declaring it using backticks.

#### Examples:

```Javascript
let str = ‘This is a string “inside” backticks’;
let str = “This is a string ‘inside’ backticks”;
let strBt = `This is a string “inside” backticks`;
```

### String Interpolation:

This is how we inject a variable into a certain part of a string.
First declare a variable using backticks and another using normal quotes.

```Javascript
let abc = “abc”;
let anotherStr = `This is a ${abc} string interpolation example.`;

console.log ( anotherStr );
// Output : This is a abc string interpolation example.
```

### String Methods:

There are many built in methods that can be used with string variables for many purposes.
Javascript strings are primitive and immutable: All string methods produces a new string without altering the original string.

#### Basic methods:

- length
- charAt()
- charCodeAt()
- at()
- [ ]
- slice()
- substring()
- substr()
- toUpperCase()
- toLowerCase()
- concat()
- trim()
- trimStart()
- trimEnd()
- padStart()
- padEnd()
- repeat()
- replace()
- replaceAll()
- split()

#### Examples:

```javascript
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;
// Output: 26
// Find the length of the string

let text1 = "Hello";
let text2 = "World!";
let text3 = text1.concat(" ", text2);
// Output: Hello World!
// Adds two string together

const url = "https://myname.com/lastname%20lastname";
console.log(url.replace("%20", "-"));
// Output: ttps://myname.com/lastname-lastname
// Replace something with another

const sepr = "my name is bingo";
console.log(sepr.split(" "));
// Get strings seperated based on a seperator.
// And it will be in a n array
// Output: [ 'my', 'name', 'is', 'bingo' ]

let text1 = "  	Hello World!      ";
let text2 = text1.trim();
// Output: Hello World!
// Cut down extra spaces

let text = "HELLO WORLD";
let char1 = text.charAt(0);
let char2 = text[0];
// Output: H
// Both return the character at a specified index (position) in a string.
```

### Search Methods:

- indexOf()
- lastIndexOf()
- search()
- match()
- matchAll()
- includes()
- startsWith()
- endsWith()

#### Examples:

```javascript
let text = "String methods used";
console.log(text.includes(“used”))
// Output: true
// search and say if something is included or not. Returns boolean value.

let text = "Please locate where 'locate' occurs!";
let index = text.indexOf("locate");
// Output: 7
// Say the first index position of that word.
```

### Number Methods:

```javascript
const number = 747;
console.log(number);

const newNumber = new Number(number);
console.log(newNumber);
// Specifically defines the type number

console.log(newNumber.toString().length);
// Convert to string and get additional string methods

console.log(newNumber.toFixed(2));
// Kind of float. Precesion values
// Output: 747.00

const precesionNum = 12.8966;
console.log(precesionNum.toPrecision(3));
// 12.9

const precesionNum2 = 124.8966;
console.log(precesionNum2.toPrecision(4));
// 124.9

const bigNum = 1000000;
console.log(bigNum.toLocaleString());
// 10,00,000
console.log(bigNum.toLocaleString("en-IN"));
// 10,00,000
// Converts a number to a string by using the current or specified locale.
```
