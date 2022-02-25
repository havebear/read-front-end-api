# String.fromCharCode()

静态 **String.fromCharCode()** 方法返回由指定的 **UTF-16** 代码单元序列创建的字符串。

``` js
console.log(String.fromCharCode(189, 43, 190, 61));
// expected output: "½+¾="
```

## 语法

``` js
String.fromCharCode(num1[, ...[, numN]])
```

## 参数

**num1, ..., numN**

一系列 UTF-16 代码单元的数字。范围介于 0 到 65535（0xFFFF）之间。大于 0xFFFF 的数字将被截断。不进行有效性检查。

## 返回值

一个长度为 N 的字符串，由 N 个指定的 UTF-16 代码单元组成。
