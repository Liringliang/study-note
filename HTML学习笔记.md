# HTML学习笔记

[TOC]

## 第一部分 HTML基本介绍

<img src="https://mdn.mozillademos.org/files/16475/element.png" alt="HTML基本格式" style="zoom:50%;" />



```
这个元素的主要部分有：

开始标签（Opening tag）：包含元素的名称（本例为 p），被左、右角括号所包围。表示元素从这里开始或者开始起作用 —— 在本例中即段落由此开始。
结束标签（Closing tag）：与开始标签相似，只是其在元素名之前包含了一个斜杠。这表示着元素的结尾 —— 在本例中即段落在此结束。初学者常常会犯忘记包含结束标签的错误，这可能会产生一些奇怪的结果。
内容（Content）：元素的内容，本例中就是所输入的文本本身。
元素（Element）：开始标签、结束标签与内容相结合，便是一个完整的元素。
```

### 第一节 基本排版

<h1>标题</h1>

```
<h1>标题</h1>
```

<p>段落Paragraph</p>

```
<p>段落Paragraph</p>
```

<p>我的猫咪脾气<strong>爆</strong>:)</p>

```
<p>我的猫咪脾气<strong>爆</strong>:)</p>
```

<em>第一</em><em>第二</em><em>第三</em>

```
<em>第一</em><em>第二</em><em>第三</em>
```

<p>第四</p><p>第五</p><p>第六</p>

```
<p>第四</p><p>第五</p><p>第六</p>
```



### 第二节 元素

元素也可以拥有属性，如下：

![&amp;amp;lt;p class="editor-note">我的猫咪脾气爆&amp;amp;lt;/p>](https://mdn.mozillademos.org/files/16476/attribute.png)

属性包含元素的额外信息，这些信息不会出现在实际的内容中。在上述例子中，这个class属性给元素赋了一个识别的名字（id），这个名字此后可以被用来识别此元素的样式信息和其他信息。

一个属性必须包含如下内容：

1. 一个空格，在属性和元素名称之间。(如果已经有一个或多个属性，就与前一个属性之间有一个空格。)
2. 属性名称，后面跟着一个等于号。
3. 一个属性值，由一对引号“ ”引起来。

### 1.图像

<img src="https://roy-tian.github.io/learning-area/extras/getting-started-web/beginner-html-site/images/firefox-icon.png" style="zoom:33%;" >

```
<img src="https://roy-tian.github.io/learning-area/extras/getting-started-web/beginner-html-site/images/firefox-icon.png" style="zoom:33%;" >
```

以上是一个空元素，即只有一个属性。

### 2.锚及其附属的属性

元素`<a>`是锚，它使被标签包裹的内容成为一个超链接。此元素也可以添加大量的属性，其中几个如下：

- `href`: 这个属性声明超链接的web地址，当这个链接被点击浏览器会跳转至href声明的web地址。例如：`href="https://www.mozilla.org/"`。
<a href=https://www.mozilla.org/>收藏页面</a>
  URL 片段是哈希标记（#）前面的名称，哈希标记指定当前文档中的内部目标位置（HTML 元素的 ID）。

  **注意:** 可以使用 `href="#top"` 或者 `href="#"` 链接返回到页面顶部。

- `title`: 标题`title`属性为超链接声明额外的信息，比如你将链接至的那个页面。例如：`title="The Mozilla homepage"`。当鼠标悬停在超链接上面时，这部分信息将以工具提示的形式显示。

- `target`: 目标`target`属性用于指定链接如何呈现出来。例如，`target="_blank"`将在新标签页中显示链接。如果你希望在当前标签页显示链接，忽略这个属性即可。

  - `_self`: 当前页面加载，即当前的响应到同一HTML 4 frame（或HTML5浏览上下文）。此值是默认的，如果没有指定属性的话。
  - `_blank`: 新窗口打开，即到一个新的未命名的HTML4窗口或HTML5浏览器上下文
  - `_parent`: 加载响应到当前框架的HTML4父框架或当前的HTML5浏览上下文的父浏览上下文。如果没有parent框架或者浏览上下文，此选项的行为方式与 `_self` 相同。
  - `_top`: IHTML4中：加载的响应成完整的，原来的窗口，取消所有其它frame。 HTML5中：加载响应进入顶层浏览上下文（即，浏览上下文，它是当前的一个的祖先，并且没有parent）。如果没有parent框架或者浏览上下文，此选项的行为方式相同_self

  **注意：**在 `<a>` 元素上使用 `target="_blank"` 隐式提供了与使用 `rel="noopener"` 相同的 `rel` 行为，即不会设置 `window.opener`。
  
  ### 3.布尔属性
  
  ```html
  <!-- 使用disabled属性来防止终端用户输入文本到输入框中 -->
  <input type="text" disabled>
  
  <!-- 下面这个输入框没有disabled属性，所以用户可以向其中输入 -->
  <input type="text">
  ```
  
  上面两段HTML代码产生的效果如下：
  <input type="text" disabled>
   <input type="text">






## 第二部分 

