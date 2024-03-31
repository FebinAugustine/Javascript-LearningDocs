# JavaScript Zero To Hero

## 01. Intermediate - Arrays

### Two types:

- Continuous
- Holey.

### Both have three variations:

- Packed SMI Elements (small integer - consist of numbers only)
- Packed Double Elements (float, NaN, Infinity)
- Packed Elements (float, string, function)

### Continuous Packed SMI:

```Javascript
	let myArr = [1, 2, 3, 4, 5]
```

An array with single data type and with no missing/null elements.

### Continuous Packed Double:

```Javascript
	let myArr = [1, 2, 3, 4, 5, 7.1];
```

An array with two data types and with no missing/null elements.

### Continuous Packed:

```Javascript
	let myArr = [1, 2, 3, 4, 5, 7.1, “a”];
```

An array with mixed data types and with no missing/null elements.

### Holey Packed SMI:

```Javascript
	let myArr = [1, 2, 3,  , 5, 6];
```

An array with a single data type and with missing/null elements.

### Holey Packed Double:

```Javascript
	let myArr = [1, 2,  , 4, 5, 7.1];
```

An array with two data types and with missing/null elements.

### Holey Packed:

```Javascript
	let myArr = [1, 2,  , 4, 5, 7.1, “a”];
```

An array with mixed data types and with missing/null elements.

- Avoid using holey arrays.
- Hierarchy of elements: SMI > Double > Packed
- Once downgraded it is not possible to upgrade the array. Even if you delete the elements.
- Checking an array with holes is expensive.
