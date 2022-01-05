# Array.from()

**Array.from()** 方法对一个类似数组或可迭代对象创建一个新的，浅拷贝的数组实例。

``` js
console.log(Array.from('foo'));
// expected output: Array ["f", "o", "o"]

console.log(Array.from([1, 2, 3], x => x + x));
// expected output: Array [2, 4, 6]

```

## 语法

Array.from(arrayLike[, mapFn[, thisArg]])

## 参数

### arrayLike

想要转换成数组的伪数组对象或可迭代对象。

### mapFn

如果指定了该参数，新数组中的每个元素会执行该回调函数。

### thisArg

可选参数，执行回调函数 mapFn 时 this 对象。

## 返回值

一个新的数组实例。

## 描述

**Array.from()** 可以通过以下方式来创建数组对象：

- 伪数组对象（拥有一个 length 属性和若干索引属性的任意对象）
- 可迭代对象（可以获取对象中的元素,如 Map和 Set 等）

Array.from() 方法有一个可选参数 mapFn，让你可以在最后生成的数组上再执行一次 map 方法后再返回。

也就是说 Array.from(obj, mapFn, thisArg) 就相当于 Array.from(obj).map(mapFn, thisArg), 除非创建的不是可用的中间数组。

## 示例

### String

``` js
Array.from('foo');
// [ "f", "o", "o" ]
```

### Set

``` js
const set = new Set(['foo', 'bar', 'baz', 'foo']);
Array.from(set);
// [ "foo", "bar", "baz" ]
```

### Map

``` js
const map = new Map([[1, 2], [2, 4], [4, 8]]);
Array.from(map);
// [[1, 2], [2, 4], [4, 8]]

const mapper = new Map([['1', 'a'], ['2', 'b']]);
Array.from(mapper.values());
// ['a', 'b'];

Array.from(mapper.keys());
// ['1', '2'];
```

### 从类数组对象（arguments）生成数组

``` js
function f() {
  return Array.from(arguments);
}

f(1, 2, 3);

// [ 1, 2, 3 ]
```


