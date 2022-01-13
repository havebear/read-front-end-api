# Promise.prototype.then()

**then()** 方法返回一个 **Promise**。它最多需要有两个参数：Promise 的成功和失败情况的回调函数。

``` js
const promise1 = new Promise((resolve, reject) => {
  resolve('Success!');
});

promise1.then((value) => {
  console.log(value);
  // expected output: "Success!"
});
```

## 语法

``` js
p.then(onFulfilled[, onRejected]);

p.then(value => {
  // fulfillment
}, reason => {
  // rejection
});
```