# 背景设置(朝右x正轴，朝下y正轴)
## 分写
### 背景颜色　background-color
background-color: 设置背景颜色,按照颜色的格式填写,比如red, #F00, rgb(255,0,0)
```html
background-color: red;
background-color: #F00;
```
### 背景图片　background-image 
```html
background-image: url("image/xxx.jpg);
```
### 背景平铺　background-repeat 
no-repeat,repeat,repeat-x,repeat-y
```html
background-repeat: repeat-x;
```
### background-attachement: 设置背景是否固定，fixed表示固定。
```html
background-attachement: fixed;
```
### 背景位置　background-position

background-position: 设置背景图片显示位置，可以使用top,bottom,left,right设置(可以组合)
```html
background-position: top left;
background-position: center center;
```
也可以直接设置数值(x轴,y轴)
```html
background-position: 10px 15px;
```
如何让一张图片达到自己想要的位置：
```
方法:
1. 设置起始位置值  background-position:0px 0px; 
2．去网页移动到自己满意的位置获取x,y值(可负值)
３．代码赋值
```
## 综合写法(顺序写，中间空格隔开)
格式：background: color image repeat position attachement;
```html
background: red url("image/xxx.png) repeat 10px 10px fixed;
```

