# Array.isArray()

**Array.isArray()** 用于确定传递的值是否是一个 Array。

``` js
Array.isArray([1, 2, 3]);
// true
Array.isArray({foo: 123});
// false
Array.isArray("foobar");
// false
Array.isArray(undefined);
// false
```

## 语法

``` js
Array.isArray(obj)
```

## 参数

### obj

需要检测的值。

## 返回值

如果值是 Array，则为true; 否则为false。

## 描述

如果对象是 Array ，则返回true，否则为false。

有关更多详细信息，请参阅文章[严格判定JavaScript对象是否为数组](https://web.mit.edu/jwalden/www/isArray.html)。

## 示例

``` js
// 下面的函数调用都返回 true
Array.isArray([]);
Array.isArray([1]);
Array.isArray(new Array());
Array.isArray(new Array('a', 'b', 'c', 'd'))
// 鲜为人知的事实：其实 Array.prototype 也是一个数组。
Array.isArray(Array.prototype);

// 下面的函数调用都返回 false
Array.isArray();
Array.isArray({});
Array.isArray(null);
Array.isArray(undefined);
Array.isArray(17);
Array.isArray('Array');
Array.isArray(true);
Array.isArray(false);
Array.isArray(new Uint8Array(32))
Array.isArray({ __proto__: Array.prototype });
```

## Polyfill

假如不存在 Array.isArray()，则在其他代码之前运行下面的代码将创建该方法。

``` js
if (!Array.isArray) {
  Array.isArray = function(arg) {
    return Object.prototype.toString.call(arg) === '[object Array]';
  };
}
```