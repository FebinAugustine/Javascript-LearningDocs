# JavaScript Zero To Hero

## 07. Basics - Objects

- Object declaration has two ways: Literal and Constructor.
- Another concept is Singleton.
- Any declaration made through a constructor that will be a constructor.
- Literal will have multiple instances and not a singleton.

### Object Literals:

```Javascript
Create empty object:
const jsUser = {};
```

Object with elements:

```Javascript
const jsUser = {
name: "bingo",
age: 24,
location: "Kochi",
isLoggedIn: false,
projects: ["pro1", "pro2"]
};
// In an object, elements are in key pair format.
```

Access an elements:

```Javascript
To access the object. Not so preferred way.
console.log(NewObject.name);
```

Another way to access object elements

```Javascript
console.log(NewObject["name"]);
```

Update an element:
To update the object. Not so preferred.

```Javascript
jsUser .name = “New”;
```

Another way to update object elements

```Javascript
NewObject["name"] = “New”;
```

Add an element:

```Javascript
jsUser .email = “jsuser@gmail.com”;
```

Add a function as an element:

```Javascript
jsUser .greet = function() {};
```

Add a nested object as an element:

```Javascript
const jsUser = {
name: "bingo",
nested: {
Contact: {
land: 0484235254,
mobile: 9497123456
}
}
};
```

Merging objects, align elements one after another.

```Javascript
let obj1 = { 1: "a", 2: "b" };
let obj2 = { 3: "c", 4: "d" };

const obj3 = Object.assign(obj1, obj2);
console.log(obj3);
```

Guarantee the array object return. {} = not a compulsory

```Javascript
const obj4 = Object.assign({}, obj1, obj2);
console.log(obj4);
```

Merging using spread operator

```Javascript
const obj5 = { ...obj1, ...obj2 };
console.log(obj5);
```

Access the keys or values of an object.
Come into use most often. Enables to loop through specifically

```Javascript
console.log(Object.keys(jsUser));
console.log(Object.values(jsUser));
```

Object Destructuring

```Javascript
const regUser = {
name: "user1",
course: "DBMS",
instructor: "Bingo",
};

// Easy access for multiple time access
const { instructor } = regUser;
console.log(instructor);

// Easy access for multiple time access
const { instructor: inst } = regUser;
console.log(inst);
```
