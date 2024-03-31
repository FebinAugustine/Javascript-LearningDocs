# JavaScript Zero To Hero

## 01. Intermediate - Bind And Object Properties

- Bind method gives access to this.
- With bind the global context converts to block context.

```Javascript
const person = {
  name: "Alice",
  greet: function() {
    console.log("Hello, my name is", this.name);
  }
};

const greetFunction = person.greet;
greetFunction();
```

- Output: Hello, my name is undefined (or window in browsers)
- greetFunction refers to the person.greet method
- Calling greetFunction directly sets this to the global object (can be different depending on strict mode)

```Javascript
const boundGreet = greetFunction.bind(person);
boundGreet();
```

- Output: Hello, my name is Alice
- Binding greetFunction to person object using bind
- Calling boundGreet ensures this refers to person object

## Object Properties:

- Built in properties of universal constants are not changeable.
- To see the object property use

```Javascript
getOwnPropertyDescription(objectName, “KeyOfTheProperty”).

  const objectProp = Object.getOwnPropertyDescription(Math, “PI”);
  console.log(objectProp );
```

- This will give you the details about the property PI in Math class.

- Here you can see that this property features like writable, enumerable and configurable are set to false hence we cannot override it.

- Likewise you can set the properties of objects you create to be not writable, enumerable and configurable.

- For that use Object.defineProperty(objectName, “KeyOfTheProperty”, {} )

#### Example:

```Javascript
let myObj = {
id: 25412
}
Object.defineProperty(myObj, “id”, {
writable: false,
enumerable: false,
configurable: false
}
```

- Now nobody will be able to override the value of the property id in your object.
- If enumerable is set to false then we cannot run loops on that particular property.
