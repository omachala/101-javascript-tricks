### Array Length

> beginner

The [Array.length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length) is a very commonly used property to get the actual length of the given array but I want to show you 2 useful concepts:

**Shortening an array** by changing the _length_ property value:

```js
const numbers = [1, 2, 3, 4];
numbers.length = 2;
numbers; // [ 1, 2 ]
```

**Create empty array of fixed length** by defining an empty array and changing the _length_ property value:

```js
const numbers = [];
numbers.length = 3;
numbers; // [ <3 empty items> ]
```

By the way another way of creating a new array with fixed length is:
```js
const numbers = new Array(3);
numbers; // [ <3 empty items> ]
```
