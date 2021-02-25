## Comma

> expert

The [comma](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comma_Operator) `,` operator enables you to create compound expression of multiple operands where the value of the last one is returned.

```js
let x = 1;
y = (x++, 100);
x; // 2
y; // 100
```

This can be handy for `reduce` array method where you want to do a simple operation and return accumulator.

```js
["a", "b", "c"].reduce((acc, char) => ((acc[char] = true), acc), {}); // { a: true, b: true, c: true }
```

You can supply multiple parameters in a `for` loop:

```js
for (let x = 0, y = 100; x <= 100; y++, y--) { ... }
```

Or define multiple variables:

```js
let a, b, c;
```
