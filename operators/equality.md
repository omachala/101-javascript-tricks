### Equality operators

> beginner

The result of evaluating an [equality operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators#equality_operators) is always of type *Boolean* based on the comparison result.

```js
"hello" == "hello"; // true
true == false; // false
true != false; // true
1 == true; // true
0 == false; // true
```

When you look at the last two examples you can notice that the results are `true` even the operands are not exactly the same. That's because the javascript engine tries to convert operands to the same type before comparing.

Because of that the recommendation is to use exclusively the [Identity](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Strict_equality) `===` and [Nonidentity](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Strict_inequality) `!==` operators.

```js
"hello" === "hello"; // true
true === false; // false
true !== false; // true
1 === true; // false
0 === false; // false
```

Let's also have a look into another interesting scenario with objects:

```js
const fruit = { name: "orange " };
const fruit2 = { name: "orange" };
fruit === fruit; // true
fruit === fruit2; // false
```

The `fruit === fruit2` returns `false` because both operands (even look the same) point to the different object (different address in the memory).
