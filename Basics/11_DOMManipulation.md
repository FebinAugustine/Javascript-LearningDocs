# JavaScript Zero To Hero

## 11. Basics - DOM Manipulation

- As you know javascript is mostly a browser based language and is associated with web development.
- DOM is a programing interface for web document.
- DOM represents documents as nodes and objects.
- Javascript is used to manipulate the DOM structure, style and content.

### Get the access to elements:

Suppose we have a HTML element and we need to manipulate it dynamically then we need the access or reference to that element.

```HTML
<h1 id=”heading” class=”title” >My Heading</h1>
```

#### For this we use:

```Javascript
let refHeading = document.getElementById("heading");

// Returns html element
let refHeading = document.getElementsByClassName("title");

// Returns HTML collection[]
let refHeading = document.getElementsByTagName("h1");

/* Return html collection[] of all elements with that tag */

let refHeading = document.querySelector("#heading");
// Returns an element

let refHeading = document.querySelector(".title");
// Returns a node list

let refHeading = document.querySelector("h1");
// Returns the first element with that tag

let refHeading = document.querySelectorAll("h1");
// Returns all the elements with that tag
```

```Javascript
document.body
```

Will give you the reference to the whole body tag of that particular html page.

```Javascript
document.documentElement
```

Will give you the reference to the whole HTML tag of that particular html page.

```Javascript
document.baseURI
```

Will give you the reference to the URL of that page

```Javascript
document.title
Will give you the reference to the title of that particular html page.
```

### Get the access to the text content:

```Javascript
 let titleContnt = document.getElementById("heading").innerHTML;
// returns the whole html text along with inline HTML tags.

let titleContnt2 = document.getElementById("heading").innerText;
// returns only the visible text

let titleContnt3 = document.getElementById("heading").textContent;
// returns the whole text but not inline tags
```

### Add an attribute into an element:

```Javascript
 let titleContnt = document.setAttribute("attribute", “value”);
//First get the reference and then use setAttribute
```

### Get an attribute from an element:

```Javascript
 let attrId = document.getAttribute(“id”);
// First get the reference and then use getAttribute
```

### Set CSS style an element:

```Javascript
 let para = document.querySelector(“p”);
para.style.backgroundColor = “green”;
// First get the reference then use style
```

### HTML document to Array conversion:

```Javascript
let refHeading = document.getElementsByClassName("title");
let doc2Arr = Array.from(refHeading);
```

### Accessing Div and its children div:

```Javascript
  const parent = document.querySelector(".week");
  console.log(parent);
  console.log(parent.children);
  console.log(parent.children[2].innerHTML);
```

### Accessing the first and last child and next sibling element:

```Javascript
 	console.log(parent.lastElementChild.innerHTML);
 	console.log(parent.firstElementChild);
console.log(parent.children[1].nextElementSibling);
```

### Node selection

```Javascript
console.log(parent.childNodes);
```

## Create an element

### div creation

```Javascript
const div = document.createElement("div");
console.log(div);
div.className = "created";
div.id = Math.round(Math.random() * 100 + 1);
Set additional attribute
div.setAttribute("title", "createdTitle");
div.style.backgroundColor = "green";
div.style.color = "black";
div.padding = "15px";
```

### Add a text node

```Javascript
let innerTxt = document.createTextNode("Hello Jango");
div.appendChild(innerTxt);
```

### Attach this newly created div into the body

```Javascript
document.body.appendChild(div);
```

### Add li item to ul

```Javascript
Create a function to add li
  function addLi(langName) {
    const li = document.createElement("li");
    li.innerText = `${langName}`;
    document.querySelector(".addLi").appendChild(li);
  }
```

### call the function to append and show

```Javascript
addLi("Python");
```

### Optimised way of the above. Avoiding traversing

```Javascript
  function addOptiLi(lang) {
    const li = document.createElement("li");
    li.appendChild(document.createTextNode(`${lang}`));
    document.querySelector(".addLi").appendChild(li);
  }
  addOptiLi("C++");
```

### Edit options in ul li in optimized way

```Javascript
  const secondLang = document.querySelector(".addLi");
  const liItem = secondLang.querySelector("li:nth-child(3)");
  const newLi = document.createElement("li");
  newLi.textContent = "Kotlin";
  liItem.replaceWith(newLi);
```

### Remove

```Javascript
const remLast = document.querySelector("li:last-child");
remLast.remove();
```
