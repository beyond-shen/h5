# 基本数据类型
## 用typeof可以返回一个值的类型

* “undefined” ——如果这个值未定义;
* “boolean” ——如果这个值是布尔值;
* “string” ——如果这个值是字符串;
* “number” ——如果这个值是数值;
* “object” ——如果这个值是对象或 null（如果定义的变量准备在将来用于保存对象,那么最好将该变量初始化为 null 而不是其他值） ;
* “function” ——如果这个值是函数。
***
typeof测试任何变量都不会报错
```html
var c;
console.log(typeof c);//"undefined"

var d = undefined;
console.log(typeof d); //"undefined"

console.log(typeof e);　//"undefined"
```
***
## 字符串(string)

1. 字符串的拼接："+"
```html
var a = "world" + "hello";
console.log(a);

console.log("html" + 123); //结果为"html123",字符串的拼接原则上时只要有一个为字符都会变成字符串
```
2. 其他类型转换成字符串的２种方法：
   * 使用toString()函数:console.log(变量名.toString());
   * 使用字符串拼接:console.log("" + 变量名);
   * 在不知道要转换的值是不是 null 或 undefined 的情况下,还可以使用转型函数 String() ,这个函数能够将任何类型的值转换为字符串。
   ```html
   var a = null;
   console.log(String(a));//null
   var b = undefined;
   console.log(String(b));//undefined
   ```
## Boolean(布尔值)
分为显式转换和隐式转换
```html
  if(a){
        console.log("........");
      }　//隐式转换代码
```
![](http://i2.muimg.com/1949/db84c96c70cb47f3.png)

## number
1. 8进制使用"0"开头,16进制，使用"0x"开头
2. 浮点数值的最高精度是 17 位小数,但在进行算术计算时其精确度远远不如整数:0.1+0.2不等于0.3而是0.30000000000000004
3. 运算和其他语言差不多，但是除法时结果为真正的商，可以带小数

### NAN

NaN ,即非数值(Not a Number)是一个特殊的数值,这个数值用于表示一个本来要返回数值的操作数未返回数值的情况(这样就不会抛出错误了)。

ECMAScript 定义了isNaN() 函数。这个函数接受一个参数,该参数可以是任何类型,而函数会帮我们确定这个参数是否“不是数值”。
```html
console.log(isNaN(10));//false
console.log(isNaN("10"));//false
console.log(isNaN("blue"));//true
console.log(isNaN("undefined"));//true
console.log(isNaN(null));//false
console.log(isNaN(NaN));//true
console.log(isNaN(true));//false

```
## 函数 function
### 定义一个函数
```html
function 函数名(){}
```
***
1. 直接用函数返回值赋值给一个变量时可以让函数出现在代码的任何一个地方－－－－函数的声明提升：函数的定义可以放在代码的任何位置，在运行时，javascript引擎
会将函数的声明提升到代码的顶部。
2. 使用赋值式定义函数时会出现错误。－－－变量声明提升：定义的变量在运行时，会被提升到代码的顶部，但是变量的赋值位置没有发生变化
```html
result = minus(10, 5);
console.log("result = ", result);


var minus = function (arg1, arg2){
    return arg1 - arg2;
};//赋值方式定义的函数
```
等价于：
```html
var minus ;
result = minus(10, 5);
console.log("result = ", result);
minus = function (arg1, arg2){
    return arg1 - arg2;
};//此时先定义了一个变量却没有给给minus赋值
```
***
### 函数传参
不像c语言传参必须一一对应，可以多传可以少传。

