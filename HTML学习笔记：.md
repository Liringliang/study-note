**HTML学习笔记：**

<img src="https://mdn.mozillademos.org/files/16475/element.png" alt="HTML基本格式" style="zoom:50%;" />

```
这个元素的主要部分有：

开始标签（Opening tag）：包含元素的名称（本例为 p），被左、右角括号所包围。表示元素从这里开始或者开始起作用 —— 在本例中即段落由此开始。
结束标签（Closing tag）：与开始标签相似，只是其在元素名之前包含了一个斜杠。这表示着元素的结尾 —— 在本例中即段落在此结束。初学者常常会犯忘记包含结束标签的错误，这可能会产生一些奇怪的结果。
内容（Content）：元素的内容，本例中就是所输入的文本本身。
元素（Element）：开始标签、结束标签与内容相结合，便是一个完整的元素。
```



<h1>标题</h1>



<p>段落Paragraph</p>

<p>我的猫咪脾气<strong>爆</strong>:)</p>

<em>第一</em><em>第二</em><em>第三</em>

<p>第四</p><p>第五</p><p>第六</p>

<img src="https://roy-tian.github.io/learning-area/extras/getting-started-web/beginner-html-site/images/firefox-icon.png">



![&amp;amp;lt;p class="editor-note">我的猫咪脾气爆&amp;amp;lt;/p>](https://mdn.mozillademos.org/files/16476/attribute.png)

```
一个属性必须包含如下内容：

1. 一个空格，在属性和元素名称之间。(如果已经有一个或多个属性，就与前一个属性之间有一个空格。)
2. 属性名称，后面跟着一个等于号。
3. 一个属性值，由一对引号“ ”引起来。
```

另一个例子是关于元素`<a>`是锚，它使被标签包裹的内容成为一个超链接。此元素也可以添加大量的属性，其中几个如下：

- `href`: 这个属性声明超链接的web地址，当这个链接被点击浏览器会跳转至href声明的web地址。例如：`href="https://www.mozilla.org/"`。
- `title`: 标题`title`属性为超链接声明额外的信息，比如你将链接至的那个页面。例如：`title="The Mozilla homepage"`。当鼠标悬停在超链接上面时，这部分信息将以工具提示的形式显示。
- `target`: 目标`target`属性用于指定链接如何呈现出来。例如，`target="_blank"`将在新标签页中显示链接。如果你希望在当前标签页显示链接，忽略这个属性即可。
