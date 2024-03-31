# JavaScript Zero To Hero

## 12. Basics - Event Handling

### Dynamically run a code block when some event occurs in the DOM.

- When a user clicks the mouse
- When a web page has loaded
- When an image has been loaded
- When the mouse moves over an element
- When an input field is changed
- When an HTML form is submitted
- When a user strokes a key

### Clicks:

```Javascript
<h1 onclick="this.innerHTML = 'Ooops!'">Click on this text!</h1>
```

#### Example:

```Javascript
<h1 onclick="changeText(this)">Click on this text!</h1>

<script>
function changeText(id) {
  id.innerHTML = "Ooops!";
}
</script>
```

### Mouse Over and Out:

```Javascript
<div onmouseover="mOver(this)" onmouseout="mOut(this)" > </div>

<script>
function mOver(obj) {
  obj.innerHTML = "Thank You"
}

function mOut(obj) {
  obj.innerHTML = "Mouse Over Me"
}
</script>
```

### Mouse Hold Down and Up:

```Javascript
<div onmousedown="mDown(this)" onmouseup="mUp(this)">
Click Me</div>

<script>
function mDown(obj) {
  obj.style.backgroundColor = "#1ec5e5";
  obj.innerHTML = "Release Me";
}
function mUp(obj) {
  obj.style.backgroundColor="#D94A38";
  obj.innerHTML="Thank You";
}
</script>
```

### On focus In & Out

```Javascript
<input type="text" onfocusin="myFunctionIn()">
<input type="text" onfocusout="myFunctionOut()">
```

## Event Listeners

```Javascript
document.getElementById("myBtn").addEventListener("click", displayDate, false);
```

- First parameter we decide what kind of event
  Second we call the function to be executed when an event happens.
- false is used to stop event bubbling

```Javascript
function displayDate() {
  document.getElementById("demo").innerHTML = Date();
}
```
