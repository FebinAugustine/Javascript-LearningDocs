# JavaScript Zero To Hero

## 01. Intermediate - Lexical Scope

```Javascript
function outer() {
	Let outrVar = “outer”;

	Function inner () {
		console.log(outrVar);
}
inner()
}
outer()
console.log(outrVar);
```

- You can see one function inside another function, one is the parent function and inside is the child function.
- As we have learned in scopes child function can access the variable declared in parent function but parents cannot access children.
- We see a log outside the parent outer function calling the variable declared inside the outer function.
- But the log will not work as it is accessing it from a global context.
- This is called Lexical scoping.
