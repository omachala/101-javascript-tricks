## Map

> intermediate

The [Map object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) holds key-value pairs and remembers the original insertion order of the keys. Any value (both objects and primitive values) may be used as either a key or a value.

The functionality of the Map object is similar to standard object - both let you set keys to values, retrieve values, delete keys and detect existing key. However, there are differences that make Map preferable in certain cases.

Advantages **Map** over standard object:

- easy getting the number of items (the `.size` property)
- keys can be any value (including functions, objects, or any primitive)
- keeps keys, and values in the order of entry insertion
- is an iterable, so it can be directly iterated
- generally better performance

```js
const cats = new Map();
cats.set("bella", { color: "ginger" }).set("daisy", { color: "black" });
cats.size; // 2
cats.has("bella"); // true
cats.get("bella"); // { color: 'ginger' }
```

**Map to array**

```js
[...cats]; // [ [ 'bella', { color: 'ginger' } ], [ 'daisy', { color: 'black' } ] ]

// or mapping to custom format:

Array.from(cats, ([name, data]) => ({ name, data }));
// [
//   { name: 'bella', data: { color: 'ginger' } },
//   { name: 'daisy', data: { color: 'black' } }
// ]
```

**Map to Object**

```js
Object.fromEntries(cats); // { bella: { color: 'ginger' }, daisy: { color: 'black' } }
```

**Iteration over Map**

```js
for (let [key, value] of cats) {
  console.log(key, value);
}

cats.forEach((value, key) => {
  console.log(key, value);
});

// for both the output is identical:
// { color: 'ginger' } 'bella'
// { color: 'black' } 'daisy'
```
