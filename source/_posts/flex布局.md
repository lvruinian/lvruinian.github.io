---
title: flex布局
---
## flex布局

display:flex;

主轴的方向（项目的排列方向）  
flex-direction：row | row-reverse | column | column-reverse

项目排列在轴线上的排列方式  
flex-wrap：nowrap | wrap | wrap-reverse
+ nowrap（默认）不换行
+ wrap 换行，第一行在上方
+ wrap-reverse 换行，第一行在下方

flex-flow是flex-direction和flex-wrap的简写，默认值为row nowrap  
flex-flow：< flex-direction > || < flex-wrap >

定义项目在主轴的对齐方式  
justify-content：flex-start | flex-end | center | space-between | space-around
+ flex-start （默认值） 左对齐
+ flex-end 右对齐
+ center 居中
+ space-between 两端对齐，项目之间间隔相等
+ space-around 每个项目两侧的间隔相等，所以，项目之间的间隔比项目与边框的间隔大一倍

定义项目在交叉轴的对齐方式  
align-items：flex-start | flex-end | center | baseline | stretch
+ flex-start 交叉轴的起点对齐
+ flex-end 交叉轴的终点对齐
+ center 交叉轴的中点对齐
+ baseline 第一行文字基线对齐
+ stretch（默认值） 如果项目未设置高度或设为auto，将占满整个容器的高度

定义多根轴线的对齐方式（若只有一根轴线，则此属性不生效）  
align-content：flex-start | flex-end | center | space-between | space-around | stretch
+ flex-start 与交叉轴起点对齐
+ flex-end 与交叉轴的终点对齐
+ center 于交叉轴的中点对齐
+ space-between 与交叉轴两段对齐，轴线之间间隔平均分布
+ space-around 每根轴线两侧的间隔都相等，所以，项目之间的间隔比项目与边框的间隔大一倍
+ stretch（默认值）轴线占满整个交叉轴

**项目的属性**

order 属性定义项目的排列顺序。数值越小，排列越靠前，默认为 0  
order:< integer >  

flex-grow 属性定义项目的放大比例，默认为 0 ，即如果存在剩余空间，也不放大  
flex-grow:< number >

flex-shrink 属性定义了项目的缩小比例，默认为1（负值无效），即如果空间不足，该项目将缩小  
flex-shrink:< number >

flex-basis 属性定义了在分配多余空间之前，项目占据的主轴空间（main size），浏览器根据这个属性，计算主轴是否有多余空间，它的默认值为auto，即项目的本来大小  
flex-basis:< length > | auto;  
可以设为width或height属性一样的值，项目将占据固定空间

flex属性是flex-grow,flex-shrink,flex-basis的简写，默认值为 0 1 auto，后两个属性可选  
flex:<'flex-grow'> <'flex-shrink'> <'flex-basis'>  
该属性有两个快捷键：auto(1 1 auto) 和 none(0 0 auto)  
建议优先使用这个属性，而不是单独写三个分离的属性，因为浏览器会推算相关值

align-self 属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-item属性，（默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch）  
align-self:auto | flex-start | flex-end | center | baseline | stretch