### Infinity

> beginner

The [Infinity](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Infinity) is simple global object representing an infinity as a numeric value. It can be used as `-Infinity` for "the lowest" possible (lower then any finite) and `Infinity` for "the highest" possible (higher then any finite) number.

A good usecase is usage of `Infinity` or `-Infinity` as starting points when number of array needs to be processed and compared:

```js
// the smallest
[8, 2, 1].reduce((smallest, num) => Math.min(smallest, num), Infinity); // 1
// the highest
[8, 2, 1].reduce((highest, num) => Math.max(highest, num), -Infinity); // 8
```

Note: The previous example is a simple demonstration of how **Infinity** works. If you really want to find the highest/smallest number in array use more performant solution:

```js
Math.min(...[8, 2, 1]); // 1
Math.max(...[8, 2, 1]); // 8
```
