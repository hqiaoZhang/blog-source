---
title: echarts 总结
date: 2017-03-14 11:18:01
tags: Echarts
---

### 1.给图片添加渐变色
#### 柱子渐变
```javascript
color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
    offset: 0,
    color: 'rgba(17, 168,171, 1)'
}, {
    offset: 1,
    color: 'rgba(17, 168,171, 0.1)'
}]),
```
<!--more-->

#### 仪表盘渐变

```javascript
// color: [[0.298, "#7d26b8"], [1, "#333946"]] //0.298是百分比的比例值（小数），还有对应两个颜色值
color: [
  [0.298, new echarts.graphic.LinearGradient(0, 0, 0, 1, [{ //添加渐变色
    offset: 0,
    color: 'rgb(130, 34,183)'
  }, {
    offset: 1,
    color: 'rgb(14, 127,214)'
  }]),], 
    [1, "#333946"]
  ]

### 2.添加图片背景

​```javascript
var PatternSrcA = './image/bgimg2.png'
var PatternImgA = new Image();
PatternImgA.src = PatternSrcA;
color: {image: PatternImgA,repeat: 'repeat'},
```