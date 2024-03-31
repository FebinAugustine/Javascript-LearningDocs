# JavaScript Zero To Hero

## 01. Intermediate - Class Constructor:

```Javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
    this.printme = function () {
      console.log(`Hello ${this.name}`);
    };
  }
  myName() {
    console.log(`My name is ${this.name}`);
  }
}

let newP = new Person("John", 41);
newP.printme();
```

### Create another class and extend:

```Javascript
class Boy extends Person {
constructor(name, age, rollNo) {
	super(name);
	super(age);
	this.rollNo = rollNo
}
}
```

- 'super' will give access to the name and age property of the parent class.
- While creating new object from this class you must use new keyword
- Use “static” keyword for restricting everyone from using methods in parent class.
