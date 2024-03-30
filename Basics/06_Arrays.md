# JavaScript Zero To Hero

## 06. Basics - Arrays

- Declare multiple items in a single variable.
- What is inside square brackets are called elements.
- Elements do not have to be of the same data type.
- Arrays are resizable.
- Zero based indexing.
- Same reference on shallow copies.

#### Creating an Array[]:

```Javascript
const myArr = [0, 1, 2, 3, true, "Name"];
```

#### Another way of creating an array:

```Javascript
const newArr = new Array(1, 2, 3, 4, 5);
```

### Methods associated with Arrays:

Add another item to the array we use push

```Javascript
const newArr2 = new Array(1, 2, 3, 4, 5);
newArr2.push(7);
console.log(newArr2);
```

Remove the last element from the array we use pop

```Javascript
newArr2.pop();
console.log(newArr2)
```

Remove the first element we use shift:

```Javascript
newArr2.shift();
console.log(newArr2);
```

Add an element to the 0 index of the array and shift the position of all other elements:

```Javascript
newArr2.unshift(8);
console.log(newArr2);
```

Boolean queries that returns true or false:

```Javascript
console.log(newArr2.includes(10));
```

Get the index of an item:

```Javascript
console.log(newArr2.indexOf(4));
```

Adds all the elements of an array into a string, separated by the specified separator string:

```Javascript
const arrayStr = newArr2.join();
console.log(newArr2);
console.log(joinArray);
console.log(typeof joinArray);
```

Slice does not include the last index in the range and does not modifies the original array:

```Javascript
console.log("A", newArr2);
const newArr3 = newArr2.slice(1, 3);
console.log(newArr3);
console.log("B", newArr2);
```

Along with including the range in full Splice modifies the original array:

```Javascript
console.log("A", newArr2);
const newArr4 = newArr2.splice(1, 3);
console.log(newArr4);
console.log("C", newArr2);
```

Add an array to another:

```Javascript
const marvelCharacter = ["char1", "char2", "char3"];
const dcCharacter = ["char4", "char5", "char6", "char7"];
marvelCharacter.push(dcCharacter);

// Output:
[ 'char1', 'char2', 'char3', [ 'char4', 'char5', 'char6', 'char7' ] ]
```

Added array is added as a single element.

To access the 4th element of the added array which is the 3rd element in the original array:

```Javascript
console.log(marvelCharacter[3][3]);
```

Another way to add an array to another array:

```Javascript
const addDc = marvelCharacter.concat(dcCharacter);
console.log(addDc);
```

First store the array in a new variable.
Concatenate returns a new array with individual elements.

Merge array Using Spread Operator:

```Javascript
const spraedArr = [...marvelCharacter, ...dcCharacter];
console.log(spraedArr);
```

Another way of merging two arrays.
Items of each array will be individualized and create a new array.
Preferred more.

Merging multiple nested array into one array we use "flat(howDeep)":

```Javascript
const nestArr = [1, 2, [7, 8, 9], [4, 5, [20, 25]]];
let flatArr = nestArr.flat(Infinity);
```

Query if something is an array:

```Javascript
console.log(Array.isArray("bingo"));
// Output: false
// Convert the return into an array:
console.log(Array.from("Hello"));
// Output: [ 'H', 'e', 'l', 'l', 'o' ]
```

When it comes to objects from() returns empty array unless specified.

```Javascript
console.log(Array.from({ name: "jango" }));
// Output: []
```

Create an array from multiple variables or any.

```Javascript
let mark1 = 50;
let mark2 = 55;
let mark3 = 58;
console.log(Array.of(mark1, mark2, mark3));

// Output: [ 50, 55, 58 ]
```
