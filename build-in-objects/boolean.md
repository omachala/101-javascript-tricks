### Boolean

> intermediate

The [Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) is an object wrapper for a boolean value. It evaluates its argument as `true` or `false`. It can be used using the `new` keyword or without.

```js
Boolean(true); // true
Boolean(0); // false
Boolean("hello"); // true
Boolean(); // false

const x = new Boolean(1);
x.valueOf(); // true
x.toString(); // 'true'
```

You can for example use the `Boolean` as a filter function:

```js
const data = ["hello", 0, undefined, "world", ""];
data.filter(Boolean); // [ 'hello', 'world' ]
```
