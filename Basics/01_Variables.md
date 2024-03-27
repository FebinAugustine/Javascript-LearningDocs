# JavaScript Zero To Hero

## 01. Basics - Variables

- Like in every other programming languages here in JS Variable are containers or boxes where we could store different types of data.
- All variables(Containers) will have a name.
- In JS to create or declare a variable we use three keywords. They are 'var', 'let' and 'const'.
- Today 'var' keyword is almost depricated and not that used.
- 'let' and 'const' are introduced in 2015.

### Variable Creation:

This is how we create a variable.

```Javascript
let myVariable = "Bingo";
const myAge = 13;
```

This has two parts. Till equal sign is the first part called declaration. From equal to end is called initialisation.

### Another way of creating a variable:

```Javascript
// Declaration:
let myVariable;

// Initialisation
myvariable = "Bingo";
```

- Use “let” if you want to change the value in future.
- Use const if the value is not intended for change, example id.
- You can name your variable anything you want but follow some naming rules.
- While naming a variable numbers are not allowed as the starting character of the variable name.

#### Example:

```Javascript
// Not allowed
const 3name = “john”;
```

- You can start with underscores, capital or small letters.
- It is preferred to use camel casing format. And try to make short variable names but be specific.

#### Example:

```Javascript
// Allowed
const userEmail = “my@email.com” ;
```

- Use a semicolon after every statement.
- Variable names are case sensitive. Even if the variable have same name if one starts with a capital and other with a small letter then they are two different variables.

```Javascript
// Allowed - Same name but two different variables
const userName = “John” ;
const Username = "Bingo"
```

Variable once declared cannot be redeclared as it will cause error. Just remember variables are containers or boxes in which we can store different types of data.
