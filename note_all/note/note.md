# `HTML5`新特性 - `Unit04`

# 1.`CanvasRenderingContext2D`

## 1.1 属性

### · `strokeStyle`

`strokeStyle`属性用于获取/设置描边颜色，其语法结构是：

```javascript

//设置
CanvasRenderingContext2D.strokeStyle = string color
//获取
variable = CanvasRenderingContext2D.strokeStyle

```

### · `fillStyle`

`fillStyle`属性用于获取/设置填充颜色，其语法结构是：

```javascript

//设置
CanvasRenderingContext2D.fillStyle = string color
//获取
variable = CanvasRenderingContext2D.fillStyle

```

### · `font`

`font`属性用于获取/设置文本样式，其语法结构是：

```javascript

//设置
CanvasRenderingContext2D.font = string font
//获取
varaible = CanvasRenderingContext2D.font

```

> `font`的结构形态与`CSS`样式中的`font`属性相同

### · `textAlign`

`textAlign`属性用于获取/设置文本水平对齐方式，其语法结构是：

```javascript

//设置
CanvasRenderingContext2D.textAlign = 'left|center|right'
//获取 
variable = CanvasRenderingContext2D.textAlign

```

## 1.2 方法

### · `strokeRect()`

`strokeRect()`方法用于绘制描边矩形，其语法结构是：

```javascript

CanvasRenderingContext2D.strokeRect(x,y,width,height)

```

### · `fillRect()`

`fillRect()`方法用于绘制填充矩形，其语法结构是：

```javascript

CanvasRenderingContext2D.fillRect(x,y,width,height)

```

### · `clearRect()`

`clearRect()`方法用于擦除画布指定区域的像素点，其语法结构是：

```javascript

CanvasRenderingContext2D.clearRect(x,y,width,height)

```

### · `strokeText()`

`strokeText()`方法用于绘制描边文本，其语法结构是：

```javascript

CanvasRenderingContext2D.strokeText(text,x,y)

```

### · `fillText()`

`fillText()`方法用于绘制填充文本，其语法结构是：

```javascript

CanvasRenderingContext2D.fillText(text,x,y)

```

## 1.3 路径

路径(`path`)，将预先定义的坐标点顺序连接所形成的图形。

路径绘制的基本步骤：

A.通过`beginPath()`方法开始一条新的路径

B.通过`moveTo()`方法来定义路径的起点

C.通过`lineTo()`、`rect()`、`arc()`等方法定义路径

D.通过`stroke()`或`fill()`方法进行描边或填充

### · `beginPath()`

`beginPath()`方法用于开始一个新的路径，其语法结构是：

```javascript

CanvasRenderingContext2D.beginPath()

```

### · `moveTo()`

`moveTo()`方法用于新的路径起点移动到指定位置，其语法结构是：

```javascript

CanvasRenderingContext2D.moveTo(x,y)

```

### · `lineTo()`

`lineTo()`方法用于使用直线连接路径的终点，其语法结构是：

```javascript

CanvasRenderingContext2D.lineTo(x,y)

```

### · `stroke()`

`stroke()`方法用于根据当前的描边样式绘制当前路径，其语法结构是：

```javascript

CanvasRenderingContext2D.stroke()

```

### · `fill()`

`fill()`方法用于根据当前的填充样式绘制当前路径，其语法结构是：

```javascript

CanvasRenderingContext2D.fill()

```

# 2. `window`对象

## ·`window.requestAnimationFrame()`

`window.requestAnimationFrame()`方法用于为浏览器定时循环操作，类似于`window.setTimeout()`，其语法结构是：

```javascript

ID window.requestAnimationFrame(callback)

```

> `window.requestAnimationFrame()`方法的优点是：
>
> A.可以充分利用显示器刷新频率(与显示器刷新频率保持一致)，所以其不会出现丢帧、卡顿现象
>
> B.如果动画页面没有处理当前标签页的话，动画将自动停止，以节省`CPU`、`GPU`资源。

## ·`window.cancelAnimationFrame()`

`window.cancelAnimationFrame()`方法用于清理由`window.requestAnimationFrame()`方法设置的`ID`，其语法结构是：

```javascript

window.cancelAnimationFrame(id)

```

作业：

通过类对于弹幕进行重构