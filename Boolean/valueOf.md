# Boolean.prototype.valueOf()

**valueOf()** 方法返回一个Boolean对象的原始值。

``` js
const x = new Boolean();

console.log(x.valueOf());
// expected output: false

const y = new Boolean('Mozilla');

console.log(y.valueOf());
// expected output: true
```

## 语法

``` js
bool.valueOf()
```

## 返回值

给定 Boolean 对象的原始值
