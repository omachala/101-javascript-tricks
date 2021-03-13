### Symbol

> expert

The [Symbol](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol) is a function which returns **symbol** which is primitive data type (like string, number, null etc.)

```js
typeof Symbol(); // 'symbol'
```

The symbol can be used as a key in object and simulate private object fields:

```js
const person = {};
const name = Symbol();
person[name] = 'Jim';
person.age = 40;
Object.keys(person); // [ 'age' ]
JSON.stringify(person); // '{"age":40}'
```

Even thought you can still access the symbol key by `Reflect.ownKeys(person)` and for the private properties you can rather use the [private class fields](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/Private_class_fields) by the hash `#` prefix.

So why the **symbol** is useful? Imagine situation you've create an object and you don't want to allow anyone to override some properties

```js
const person = {};
let name = Symbol('name');
person[name] = 'Jim';

// creating new symbol with the same name
name2 = Symbol('name');
person[name2] = 'James';

person[name2]; // 'James'
person[name]; // 'Jim'
```

Even I created a new symbol with the same name I wasn't been able to override the existing object in field that's bause the `Symbol` function always returns unique value.
