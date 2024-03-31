# JavaScript Zero To Hero

## 01. Intermediate - Get & Set

Get and Set is a method put on properties to override some properties.

### Class Based:

```Javascript
class user {
	constructor(email, password) {
		this.email = email;
		this.password = password;
},

set password( value ) {
	this._password = value;
},
get password( ) {
	return this._password.toUpperCase();
}
}
```

### Function Based:

```Javascript
function User( email, password ) {
	this._email = email;
	this._password = password;

	Object.defineProperty(this, password, {
		set: function ( value ) {
			this.password = value;
},
get: function ( ) {
	return this._password.toUpperCase();
},
});
```

### Object Based:

```Javascript
const user = {
	_email: “emial@mail.com”,
	_password: “lkj123”,

	set password ( value ) {
		this._password = value;
},
get password ( ) {
		return this._password.toUpperCase();
}
}
```
