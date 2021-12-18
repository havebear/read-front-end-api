# String.prototype.trim

trim() 方法会从一个字符串的两端删除空白字符。在这个上下文中的空白字符是所有的空白字符 (space, tab, no-break space 等) 以及所有行终止符字符（如 LF，CR等）。

## 语法

``` js
const str = ' Hello world   '
str.trim()
// Hello world
```

## 返回值

一个代表调用字符串两端去掉空白的新字符串。（不会改变自身）

## Polyfill

``` js
if (!String.prototype.trim) {
  String.prototype.trim = function () {
    return this.replace(/^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g, '');
  };
}
```
