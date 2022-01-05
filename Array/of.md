# Array.of()

**Array.of()** 方法创建一个具有可变数量参数的新数组实例，而不考虑参数的数量或类型。

``` js
Array.of(7);       // [7]
Array.of(1, 2, 3); // [1, 2, 3]

Array(7);          // [ , , , , , , ]
Array(1, 2, 3);    // [1, 2, 3]
```

## 语法

``` js
Array.of(element0[, element1[, ...[, elementN]]])
```

## 参数

### elementN

任意个参数，将按顺序成为返回数组中的元素。


## 返回值

新的 **Array** 实例。

## 描述

此函数是ECMAScript 2015标准的一部分。

## 示例

``` js
Array.of(1);         // [1]
Array.of(1, 2, 3);   // [1, 2, 3]
Array.of(undefined); // [undefined]
```

## 兼容性

``` js
if (!Array.of) {
  Array.of = function() {
    return Array.prototype.slice.call(arguments);
  };
}
```
