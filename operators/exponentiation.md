### Exponentiation operator

> beginner

The [exponentiation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Exponentiation) operator (\*\*) is a shortcut of the `Math.pow` function (except it also accepts BigInts as operands) and returns the result of raising the first operand to the power of the second operand

```js
2 ** 3; // 8 (2 * 2 * 2)
4 ** 5; // 1024
2 ** (3 ** 2); // 512
```

Similar is [exponentiation assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Exponentiation_assignment) `**=` which raises the value of a variable to the power of the right operand.

```js
let a = 2;
a **= 4; // 16
```
