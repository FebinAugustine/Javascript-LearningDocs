# JavaScript Zero To Hero

## 05. Basics - Dates

#### Let's learn how to use dates.

```Javascript
let myDate = new Date();
console.log(typeof myDate);
// Date is a type object

const myNewDate2 = new Date();

// GET Date
console.log(myNewDate2.getDate());
console.log(myNewDate2.getMonth());
console.log(myNewDate2.getFullYear());
console.log(myNewDate2.getDay());
// OUTPUT:
// 17
// 2
// 2024
// 0

// GET Time
console.log(myNewDate2.getHours());
console.log(myNewDate2.getMinutes());
console.log(myNewDate2.getSeconds());
console.log(myNewDate2.getMilliseconds());
// OUTPUT:
// 19
// 2
// 33
// 252

// to methods
console.log(myNewDate2.toDateString());
console.log(myNewDate2.toTimeString());
console.log(myNewDate2.toLocaleString());
console.log(myNewDate2.toLocaleDateString());
console.log(myNewDate2.toLocaleTimeString());
// OUTPUT:
// Sun Mar 17 2024
// 19:06:05 GMT+0530 (India Standard Time)
// 17/3/2024, 7:06:05 pm
// 17/3/2024
// 7:06:05 pm

// to UTC methods
console.log("to UTC methods");
console.log(myNewDate2.toUTCString());
console.log(myNewDate2.getUTCDate());
console.log(myNewDate2.getUTCHours());
console.log(myNewDate2.getTimezoneOffset());
console.log(myNewDate2.toJSON());
// OUTPUT:
// Sun, 17 Mar 2024 13:54:50 GMT
// 17
// 13
// -330
// 2024-03-17T13:54:50.872Z
```
