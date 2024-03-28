# JavaScript Zero To Hero

## 03. Basics - Operators

Now we know variables and data types, let's move on to operators.

### Widely used operators:

- Assignment Operators
- Arithmetic Operators
- Comparison Operators
- Logical Operators
- Type Operators
- Ternary Operators
- Nullish Coalescing Operator

### Assignment Operators

These are used to assign something to something.

#### Operators:

=, +=, -=, \*=, /=, %=, \*\*=

#### Example:

```Javascript
	let x = 22;
	X += 10;
	console.log(x);  // Output: 32
```

### Arithmetic Operators

These are used to do mathematical functions like adding, subtracting, multiplication, etc..

#### Operators:

    +, -, *, /, **, %, ++, - -

#### Examples:

```Javascript
let num1 = 10;
let num2 = 5;
Let numTotal = num1 + num2;
```

- Operator + used with string data types is called "concatenation".
- Because JS is line by line and from left to right type preference matters.

#### Example:

```Javascript
“Num” + 16 + 2
/* output will be Num162. Data type first variable data type is assigned to other number.*/

12 + 10 + “Num” // output will be: 22Num
```

### Comparison Operators:

These are used to compare two things.

#### Operators:

```Javascrip
==, ===, !=, !==, <, >, <=, >=, ?
```

### Logical Operators

Logical operators are used to determine the logic between variables or values.

#### Operators

```Javascrip
&& , || , !
```

### Type Operators

Used to know the data type of something or instance of something.

#### Operators:

typeof,
instanceof

### Conditional (Ternary) Operator

JavaScript also contains a conditional operator that assigns a value to a variable based on some condition.

#### Operator:

?

```Javascrip
let valName = (condition) ? value1:value2
```

### Nullish Coalescing Operator

#### Operator:

??

The ?? operator returns the first argument if it is not nullish (null or undefined).
Otherwise it returns the second argument.

#### Example:

```Javascript
let name = null;
let text = "missing";
let result = name ?? text;
```
