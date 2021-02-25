## IN

> intermediate

The [in](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/in) operator returns true/false if the specified property exists in the given object:

```js
"a" in { a: 1 }; // true
"b" in { a: 1 }; // false
```

For the arrays the array index is considered as a property:

```js
"b" in ["a", "b"]; // false
1 in ["a", "b"]; // true
```
