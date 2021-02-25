### Delete

> beginner

The [delete](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete) operator deletes an object's property.

If the operation is possible then `true` is returned and object is modified inplace. The `false` is returned if operation failed.

```js
const obj = { a: 1, b: 2 };
delete obj.a; // true
obj; // { b: 2 }
```

It's also technically possible to use it for arrays by pointing the index (since arrays are just objects) but it keeps the original array length and it's generally a bad practice - use array methods instead.

```js
// !! avoid this usage !!
const arr = [1, 2, 3];
delete arr[1]; // true
arr; // [ 1, <1 empty item>, 3 ]
arr.length; // 3
```
