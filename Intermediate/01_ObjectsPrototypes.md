# JavaScript Zero To Hero

## 01. Intermediate - Objects & Prototypes

### OOP’s

- JavaScript is a unique case in the world of OOP.
- Traditionally OOP relies on classes for object creation and inheritance.
- Instead of classes having properties and methods JS have objects with the same.
- JavaScript utilizes prototypes for inheritance.
- A JS file in itself is an object.
- In standalone runtime environment it has an empty object, in browser it has a window object

### Objects:

- Instead of classes JS uses objects with default properties and methods.
- Objects act as blueprints for creating instances with similar characteristics.

### Prototype:

- Every object has a hidden property called prototype.
- Prototype acts as the source of inheritance hence called prototypal inheritance
- Accessing an object property JS checks the object itself first then the prototype till it reaches null.
- Prototype is a kind of Parent which the object inherits from.

### Object Creation:

#### Object Literals:

Define objects with key value pairs as properties and methods.

```Javascript
const person = {
  name: "Rob",
  age: 30,
  greet() {
    console.log("Hello, my name is", this.name);
  },
};

let person1 = Object.create(person);
person1.name = "Manu";
person1.greet();
```

- 'this' refers to current context.
- In this example, person1 inherits the greet method from the person prototype.

### Constructor functions:

- In JavaScript, constructor functions are regular functions designed to be invoked with the new keyword. When called with new, they create a new object, initialize it with properties and methods, and implicitly return it.
- Provides a structured approach to creating objects with shared properties and methods.
- It's a convention to name constructor functions with a capital letter at the beginning to distinguish them from regular functions.

#### Example:

```Javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
    this.greet = function () {
    console.log("Hello, my name is", this.name);
    console.log("Hello, my age is", this.age);
    };
}

  const person1 = new Person();
  person1.name = "John";
  person1.age = 18;
  person1.greet();
```

## Prototype Injection and this & new keywords:

- At the end everything including array and function is an object.
- Every object has a prototype.
- Through the prototype we can access additional methods of parent.

### Inject into a Constructor function:

```Javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.printMe =  function () {
    console.log(`Hello ${this.name}`);
  }
}

Person.prototype.myName = function () {
  console.log(`My name is ${this.name}`);
};

let newP = new Person("John", 41);
newP.myName();
```

- Must use a new keyword while creating a new object from the parent.
- 'new' keyword initiates the creation of a new object.
- Must use this keyword to get the current context

### Inject into the base Object:

```Javascript
Object.prototype.myName = function () {
  console.log(`My name is ${this.name}`);
};
```

This is considered a base Object. As everything is an object all will get the access to this function.
