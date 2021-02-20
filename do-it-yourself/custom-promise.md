## Custom Promise

```js
class MyPromise {
  resCb = () => {}
  rejCb = () => {}
  finallyCb = () => {}
  constructor(callback) {
    const res = (data) => (this.resCb(data), this.finallyCb(data))
    const rej = (data) => (this.rejCb(data), this.finallyCb(data))
    callback(res, rej)
  }
  then(cb) {
    this.resCb = cb
    return this
  }
  catch(cb) {
    this.rejCb = cb
    return this
  }
  finally(cb) {
    this.finallyCb = cb
    return this
  } 
}
```

And usage:

```js
const promise = new MyPromise((res) => setTimeout(() => res('hello world'), 1000))
promise.then(console.log).finally(console.log)
```

Or async/await syntax:

```js
const run = async () => {
  const promise = new MyPromise((res) => setTimeout(() => res('hello world'), 1000))
  const res = await promise
  console.log(res)
}
```
