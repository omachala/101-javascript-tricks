### Stric mode

> expert

[Strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode) has been introduced in ECMAScript 5 and allows you to place a program, or a function, in a “strict” operating context. It was also designed in the hope that developers who limit themselves to strict mode would make fewer mistakes leading to bugs.

To invoke strict mode for an entire script, put the exact statement `"use strict";` before any other statements. The very beginning of the file or function body.

Example:
```js
myVar = "hello world"; // This will not cause an error.

function myFunction() {
  "use strict";
  myVar = "hello world"; // This will cause an error (myVar is not defined).
}

myFunction();
```

The NodeJS uses [CommonJS](https://nodejs.org/api/modules.html#modules_modules_commonjs_modules) modularization by default so you don't need to use strict mode in any of your files.

Since the introduction of ECMAScript 2015, you don’t have to include the 'use strict'; statement when writing JavaScript modules to enable strict mode.
