# Assertions 

Assertion is used to check the result of a computation, It'll throw and error if the expected result is not valid.
This is only available with Node API and no available on the client side (browser)
```js
assert.equal(7 + 1, 8);
```

assert.deepEqual is used to compare objects deeply. Will check all nested values too.

```js
// This is required
var assert = require('assert');

const assertObject = {
    _id: "638bffdeb49097780395f263",
    index: 0,
    guid: "9845474e-f1a0-4322-ac87-973a81a3a9c0",
    isActive: true,
    balance: "$1,513.52",
    picture: "http://placehold.it/32x32",
    name: {
      first: "John",
      middle: "Carmen",
      last: "Doe"
    }
  }
  
  const assertCompareObject = {
    _id: "638bffdeb49097780395f263",
    index: 0,
    guid: "9845474e-f1a0-4322-ac87-973a81a3a9c0",
    isActive: false,
    balance: "$1,513.52",
    picture: "http://placehold.it/32x32",
    name: {
      first: "John",
      middle: "Carmen",
      last: "Doe"
    }
  }
  
console.log(assert.deepEqual(assertCompareObject, assertObject))
  

```
