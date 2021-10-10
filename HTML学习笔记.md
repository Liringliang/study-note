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

```html
<p>第四</p><p>第五</p><p>第六</p>
```

**注释**

```html
<!--注释-->
```



### 第二节 元素

### 1.常见元素

**（1）**

`main`	让搜索引擎和开发者能很快地找到网页的主要内容。

​			举例：

```html
<main> 
  <h1>Hello World</h1>
  <p>Hello Paragraph</p>
</main>
```

`header`	页首

`footer	`	页脚

`nav	`

`video`	`article	`	

`section	`	

**（2）元素也可以拥有属性，如下：**

![&amp;amp;lt;p class="editor-note">我的猫咪脾气爆&amp;amp;lt;/p>](https://mdn.mozillademos.org/files/16476/attribute.png)

属性包含元素的额外信息，这些信息不会出现在实际的内容中。在上述例子中，这个class属性给元素赋了一个识别的名字（id），这个名字此后可以被用来识别此元素的样式信息和其他信息。

一个属性必须包含如下内容：

1. 一个空格，在属性和元素名称之间。(如果已经有一个或多个属性，就与前一个属性之间有一个空格。)
2. 属性名称，后面跟着一个等于号。
3. 一个属性值，由一对引号“ ”引起来。



### 2.图像

```html
<img src="https://www.freecatphotoapp.com/your-image.jpg">
```

`img`	表示图片元素，`src`	属性表示指向图片的地址，没有结束标签。

所有的 `img` 元素 **必须** 有 `alt` 属性。 `alt` 的属性值有两个作用，第一个作用是让屏幕阅读器可以知晓图片的内容，这会对网页的可访问性有很大提升；另一个作用是当图片无法加载时，页面需要显示的替代文本。

```html
<img src="https://www.freecatphotoapp.com/your-image.jpg" alt="A business cat wearing a necktie.">
```
<img src="https://www.freecatphotoapp.com/your-image.jpg" alt="A business cat wearing a necktie." style="zoom:25%;" >


### 3.锚及其附属的属性

元素`<a>`是锚（Anchor，简写为 a），它使被标签包裹的内容成为一个超链接。此元素也可以添加大量的属性，其中几个如下：

- `href`	点击链接后指向跳转的目的地，四个功能：

  **功能一：用 a 实现网页间的跳转**

  ```html
  <a href="https://www.freecodecamp.org">this links to freecodecamp.org</a>
  ```
  <a href="https://www.freecodecamp.org">this links to freecodecamp.org</a>

  

  **功能二：用 a 实现网页内部跳转**

  创建内部链接，跳转到网页内的各个不同部分。

  要创建内部链接，你需要将链接的 `href` 属性值设置为一个哈希符号 `#` 加上你想内部链接到的元素的 `id`，通常是在网页下方的元素。 然后你需要将相同的 `id` 属性添加到你链接到的元素中。 `id` 是描述网页元素的一个属性，它的值在整个页面中唯一。

  当用户点击了 `Contacts` 链接，页面就会跳转到网页的 **Contacts** 区域。

  ```html
  <a href="#contacts-header">Contacts</a>
  ...
  <h2 id="contacts-header">Contacts</h2>
  ```

  效果：
  
  <a href="#contacts-header">Contacts</a>
  ...

  <h2 id="contacts-header">Contacts</h2

  **注：**如果要实现页面头部和尾部的跳转，可以设置`id`值为`header``footer`
  
  ```html
  <a href="#footer">跳转至尾部</a>
  ...
  <h2 id="footer">尾部</a>
  ```
  
  效果：
  
  <a href="#footer">跳转至尾部</a>
  ...

  <h2 id="footer">尾部</a>

  **功能三：将 a 嵌套在段落中**
  
  可以在其他文本元素内嵌套链接。
  
  ```html
  <p>
    Here's a <a target="_blank" href="https://www.freecodecamp.org"> link to www.freecodecamp.org</a> for you to follow.
  </p>
  ```

  `target` 是锚点元素的一个属性，它用来指定链接的打开方式。 属性值 `_blank` 表示链接会在新标签页打开。 `href` 是锚点元素的另一个属性，它用来指定链接的 URL。  `a` 元素内的文本 `link to www.freecodecamp.org` 叫作锚文本，会显示为一个可以点击的链接：

  Here's a [link to www.freecodecamp.org](https://www.freecodecamp.org/) for you to follow.

**功能四：用#号来创建链接占位符**

有时你想为网站添加一个 `a` 元素，但还不确定要将它链接到哪里。

当你使用 `JavaScript` 更改链接的指向时，这也很方便，我们将在后面的课程中介绍。

例如: `href="#"`

- `title`: 标题`title`属性为超链接声明额外的信息，比如你将链接至的那个页面。例如：`title="The Mozilla homepage"`。当鼠标悬停在超链接上面时，这部分信息将以工具提示的形式显示。

- `target`: 目标`target`属性用于指定链接如何呈现出来。例如，`target="_blank"`将在新标签页中显示链接。如果你希望在当前标签页显示链接，忽略这个属性即可。

  - `_self`: 当前页面加载，即当前的响应到同一HTML 4 frame（或HTML5浏览上下文）。此值是默认的，如果没有指定属性的话。
  - `_blank`: 新窗口打开，即到一个新的未命名的HTML4窗口或HTML5浏览器上下文
  - `_parent`: 加载响应到当前框架的HTML4父框架或当前的HTML5浏览上下文的父浏览上下文。如果没有parent框架或者浏览上下文，此选项的行为方式与 `_self` 相同。
  - `_top`: IHTML4中：加载的响应成完整的，原来的窗口，取消所有其它frame。 HTML5中：加载响应进入顶层浏览上下文（即，浏览上下文，它是当前的一个的祖先，并且没有parent）。如果没有parent框架或者浏览上下文，此选项的行为方式相同_self

  **注意：**在 `<a>` 元素上使用 `target="_blank"` 隐式提供了与使用 `rel="noopener"` 相同的 `rel` 行为，即不会设置 `window.opener`。
  
  

### 4.布尔属性

```html
<!-- 使用disabled属性来防止终端用户输入文本到输入框中 -->
<input type="text" disabled>

<!-- 下面这个输入框没有disabled属性，所以用户可以向其中输入 -->
<input type="text">
```

上面两段HTML代码产生的效果如下：
<input type="text" disabled>
<input type="text">

### 5.

### 6.

### 7.

### 8.



## 第二部分 

