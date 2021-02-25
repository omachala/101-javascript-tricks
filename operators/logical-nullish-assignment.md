### Logical nullish assignment

> expert

The [logical nullish assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_nullish_assignment) operator **?==** only assigns value to an object property if it does not exists (is `undefined`) or has `null` value (=nullish).

```js
const person = { name: "Alice" };

person.name ??= "Bob";
person; // { name: 'Alice' }

person.age ??= "30";
person; // { name: 'Alice', age: '30' }
```
