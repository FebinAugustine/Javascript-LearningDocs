# JavaScript Zero To Hero

## 01. Intermediate - Async Fetch

```Javascript
async function asyncFetch() {
	try {
		const response = await fetch(http://github.in/users);
		const data = await response.json;
		console.log( response );
}catch(err) {
	console.log(“Error:”, err);
}
}

asyncFetch()
```

## Fetch and .then

- Micro task.
- Priority que

```Javascript
fetch(http://github.in/users)
.then((res)=>{
return res.json();
})
.then((data)=>{
console.log(“data”);
})
.catch(( error )=> error)
```
