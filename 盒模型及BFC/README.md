# CSS盒模型


## 基本概念 ： 标准模型 + IE 模型
#### 标准模型与 IE 模型的区别 ： 宽高的计算方式不同
#### 标准模型宽高 ： 不包括 padding 和 border，只是 content 的宽高
#### IE 模型宽高 ：宽高包含 padding 和 border
#### 标准模型 box-sizing：content-box （浏览器默认）
#### IE模型 box-sizing：border-box


## ＪＳ获取宽高
#### 1. dom.style.width/hright => 只能获取内联样式的宽高
#### 2. dom.currentStyle.width/height => 获取渲染以后的样式，缺点：只有 IE 支持
#### 3. window.getComputedStyle(dom).width/height => 获取渲染以后的样式，优点：通用的，兼容性好
#### 4. document.getBoundinngClientRect().width/height => 根据视口得到四个值，left top width height


## BFC : 块级作用域上下文
### 原理：
#### 1. 在 BFC 这个元素垂直的方向发生重叠
#### 2. BFC 的区域不会与浮动元素的 box 重叠 （用来清除浮动）
#### 3. BFC 在页面上是个独立的容器，外面的元素不会影响里面的元素，里面的元素也不会影响外面的元素
#### 4. 计算 BFC 的高度时，浮动元素也会参与就算


## 如何创建 BFC
#### 1. float 的值不为 none
#### 2. position 值只要不是 static/relative
#### 3. display 属性值是与 table 相关的
#### 4. overflow:hidden/auto


