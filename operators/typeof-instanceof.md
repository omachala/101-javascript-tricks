### typeof vs instanceof

> intermediate

Both [typeof](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof) and [instanceof](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/instanceof) identify the type of a value but the difference is that:

- **typeof** returns alway string like `"number"`, `"string"`, `"boolean"` or `"undefined"` indicating the type of the operand
- **instanceof** stands for constructors (functions, classes) and returns `true` if the value is a child of the right-hand-side callable object

```js
class Car {}
class Animal {}
class Fish extends Animal {}
const nemo = new Fish();

nemo instanceof Object; // true
nemo instanceof Animal; // true
nemo instanceof Fish; // true
nemo instanceof Car; // false
nemo instanceof nemo; // TypeError: Right-hand side of 'instanceof' is not callable

typeof nemo; // 'object'
typeof Animal; // 'function'
typeof 12; // 'number'
typeof something; // 'undefined'
```
