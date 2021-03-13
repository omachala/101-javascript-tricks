### new.target

> expert

The [new.target](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new.target) pseudo function property (only exists within functions) stands for detecting whether the function has been invoked using the `new` operator.

```js
function Animal(name) {
  if (new.target) {
    throw new TypeError("Animal is not a constructor.");
  }
  console.log(name);
}

new Animal("giraphe"); // TypeError: Animal is not a constructor.
Animal("giraphe"); // 'giraphe'
```

This is useful in cases when you don't want to allow invoking your function using the `new` keyword as it might not be a useful or legal usage. This can of course be used vice versa `if (!new.target)` and require invoking your function only by using the `new` keyword.
