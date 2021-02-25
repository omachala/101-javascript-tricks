### Void

> expert

The [void](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/void) is unary operator evaluates the given expression and then returns `undefined`.

You can create an immediately-invoked function and force it to be forgotten (the function keyword to be treated as an expression instead of a declaration).

```js
void function myFunction() {
  console.log('myFunction has been executed!');
}(); // 'myFunction has been executed!'

myFunction; // ReferenceError: myFunction is not defined
myFunction(); // ReferenceError: myFunction is not defined
```
