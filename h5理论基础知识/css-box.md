# Css盒子

![](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1492400663224&di=a58a0e9791b6b539b99a41f6d886fb11&imgtype=0&src=http%3A%2F%2Fwww.dnzg.cn%2Fuploads%2Fallimg%2F140511%2F21302aU8-3.png)
## 盒子计算

* Width = border-left+padding-left+width+padding-right+border-right.
* Height = border-top+padding-top+height+padding-bottom+border-bottom.

## 边框属性

### 边框宽度：
* border-top-width：上边框宽度
* border-right-width：右边框宽度
* border-bottom-width：下边框宽度
* border-left-width：左边框宽度
* border-width：上边框宽度[右边框宽度 下边框宽度 左边框宽度]

### 边框样式

* border-top-style:上边框样式
* border-right-style:右边框样式
* border-bottom-style:下边框样式
* border-left-style:左边框样式
* border-style:上边框样式 [右边框样式 下边框样式 左边框样式]
* 常用样式: solid(实线) dashed(虚线) dotted(点状边框) double(双实线)

### 边框颜色

* border-top-color:上边框颜色
* border-right-color:右边框颜色
* border-bottom-color:下边框颜色
* border-left-color:左边框颜色
* border-color:上边框颜色 [右边框颜色 下边框颜色 左边框颜色] 
***
__注意__：设置边框颜色时同样必须设置边框样式，如果未设置样式或设置为none，边框颜色无效。
***

### 综合设置

边框属性的综合设置:
```html
border-top: 宽度 样式 颜色
border-top: 1px solid red;
border: 宽度 样式 颜色
border: 1px dotted yellow;
```
***
小技巧：border: 0 none; 设置边框为0的方法。
***

## 边距问题
### 内边距 padding

* padding-top: 上内边距
* padding-right: 右内边距
* padding-bottom: 下内边距
* padding-left: 左内边距

**注意**：修改padding会影响盒子的大小

### 外边距 margin

* margin-top: 上外边距
* margin-right: 右外边距
* margin-bottom: 下外边距
* margin-left: 左外边距

### 综合设置
1. 特殊用法：取消浏览器所有默认属性
```html
*{
margin:0;
padding:0;
}
```
2. 综合设置：padding/margin：上内边距[右内边距 下内边距 左内边距]

        1. 1个属性值：所有都一样
        2. 2个属性值：上下-左右
        3. 3个属性值：上-左右-下
        4. 4个属性值：上-右-下-左
***
 小技巧 ：（auto只是作用于左右对上下没影响）
 1. margin: 10px auto; 实现盒子在父盒子中的水平居中
 2. margin-top:指定属性值  实现盒子在父盒子中的垂直居中
 3. .外边距可以使用负值，使相邻元素重叠。
 4. **外边距合并**情况：（1）2个处于同一父盒子里面的**上下**子盒子，外边距等于2者外边距中的**最大值** （2） 2个处于同一父盒子里面的**左右**盒子，外边距为2者外边距的**和** ）（3） 对于**嵌套关系**的2个块元素，如果父元素**没有上内边距及边框**，则父元素的上外边距会与子元素的上外边距发生合并，合并后的外边距为两者中的**较大者**，即使父元素的上外边距为0，也会发生合并。即子元素中的外边距会影响到父元素。
 5. 解决嵌套关系中的合并问题：（1) padding:1px （2） border:1px solid red;
***
