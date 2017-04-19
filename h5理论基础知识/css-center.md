# 关于居中问题的方法介绍

## 文本内容的居中
1. 文本的水平居中
```html
text-align:center;
```
2. 文本内容的垂直居中
```html
line-height:height的值;
```
## 盒子的居中

### margin法:
1. 水平居中
```html
margin:0px auto;
```
2. 垂直居中
```html
margin:一定的像素值(可计算);
```

### padding法:
***
**注意事项**：由于padding的使用会改变盒子的大小，所以使用时要变化你设定的原大小，使用方法同margin
***

### 常用法：position

1. 固定设置法：缺陷是在父元素不清楚无法使用
```html
position:(relative/absolute);
top:计算值；
left:计算值;
```
2. 百分比法：父元素属性不清楚可用
```html
举列垂直居中（水平居中类似的）
top:50%;------相对于父元素的百分比
margin-top: -50px----向上移动元素本身高度的一半
      }
```
