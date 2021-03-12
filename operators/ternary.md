### Ternary

> beginner

The [ternary operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) takes three operands and is basically a shortcut for the [if](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else) statement.

```js
let result = 1 === 1 ? "equal" : "not equal";
result; // 'equal'

// Is the same as:

if (1 === 1) {
  result = "equal";
} else {
  result = "not equal";
}
result; // equal
```

The ternary operator can be chained which is equivalent to `if … else if … else` statement chain:

```js
const x = 3;
const y = x == 1 ? 1 : x == 2 ? 2 : x == 3 ? 3 : "more than 3";
y; // 3
```
