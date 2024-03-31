# JavaScript Zero To Hero

## 01. Intermediate - Closure

```Javascript
function makeFunc() {
  const name = "Mozilla";
  function displayName() {
  	console.log(name);
  }
  return displayName;
}

const myFunc = makeFunc();
myFunc();
```

- Unlike in lexical scoping function here we are returning the inner function.
- Inner has not been executed yet.
- But we called the outer function and got executed.
- The return is still in the memory.
- Now if we access that return the entire inner and outer scope together get called again.
- This is called Closure.
