### Optional Chaining

> beginner

The [optional chaining](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining) (**?.**) operator allows you to read values deeply nested within a chain of connected objects even when any of nested object can be `null` or `undefined`.

Consider following object:

```js
const person = {
  name: "Alice",
};
console.log(person.address.street.number); // TypeError: Cannot read property 'street' of undefined
```

To avoid the error you normally need to use some conditional expression:

```js
if (person.address && person.address.street && person.address.street.number) {
  console.log(person.address.street.number);
}
// or
person.address && person.address.street && person.address.street;
```

Using the optional chaining you can simply do:

```js
person.address?.street?.number; // undefined
```

Using optional chaining with method calls automatically returns `undefined` instead of throwing an exception:

```js
person.getAge(); // TypeError: person.getAge is not a function
person.getAge?.(); // undefined
```
