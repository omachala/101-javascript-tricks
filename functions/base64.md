### Base64

> intermediate

Base64 is a group of encoding schemed to allow represent binary data in an ASCII string format (character set very widely supported by any computer system) by translating the data into a radix-64 representation. This is very useful everywhere you need to transfer the data as text without loss or modification.

In JavaScript there are two functions respectively for decoding and encoding base64 strings:

1. **`btoa()`** creates a base-64 encoded ASCII string from a "string" of binary data 
2. **`atob()`** decodes a base64 encoded string

Encode object to base64 string:
```js
const myObject = { a: 1, b: 2 };
// serialize object to string
const json = JSON.stringify(myObject)
// make base64 representation
btoa(json); // 'eyJhIjoxLCJiIjoyfQ=='
```

Decode base64 string to object:
```js
const json = atob('eyJhIjoxLCJiIjoyfQ=='); // '{"a":1,"b":2}'
const myObj = JSON.parse(json);
myObj; // { a: 1, b: 2 }
```


