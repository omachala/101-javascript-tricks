### Spread operator

> beginner

[Spread operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax) is extremely common and useful syntax allows you inplace expand iterables (array, object, string, ...). The most common usage is "concatenating" arrays and objects:

```js
const obj = { a: 1, b: 2 };
{ ...obj, c: 3 }; // { a: 1, b: 2, c: 3 }
{ ...obj, a: 3 }; // { a: 3, b: 2 }
{ a:3, ...obj }; // { a: 1, b: 2 }

const arr = [ 1, 2 ];
[ ...arr, 5, 6 ]; // [ 1, 2, 5, 6 ]
```

_Please note: Spread operator may NOT be appropriate for object copying as it's doing shallow copy only. This means it duplicates only the top-level properties, but the nested objects still keep their original references._

**Rest syntax (parameters)** which is the opposite of spread syntax - collects multiple values (function arguments) into array:

```js
function favouriteFruits(...fruits) {
  console.log(fruits.join(", "));
}

favouriteFruits("banana", "apple", "mango"); // 'banana, apple, mango'
```
