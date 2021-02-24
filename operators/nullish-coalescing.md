### Nullish coalescing

> intermediate

The [Nullish coalescing](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_operator) operator returns the right-hand side of the operand only if the left-hand operand is `null` or `undefined`. This is useful when you work with numbers and do not want to consider zero `0` as an invalid value or for strings where empty string `""` can still be considered as a valid value.

The widely used logical OR **||** operator can't be sometimes properly used for numbers and strings:

```js
const childAge = 0;
console.log(`Child age is ${childAge || "---"} years`); // 'Child age is --- years'
console.log(`Child age is ${childAge ?? "---"} years`); // 'Child age is 0 years'
```
