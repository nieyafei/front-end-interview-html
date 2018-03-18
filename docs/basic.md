# Font-end-interview-html
前端面试interview的HTML题目收集，必看题目

## HTML和XHTML的区别 ☆
**什么是HTML?**
> Html是用来描述网页的一种语言，是一切网页的基础。
> - HTML 指的是超文本标记语言 (Hyper Text Markup Language)
> - HTML 不是一种编程语言，而是一种标记语言
> - 标记语言是一套标记标签 (markup tag)
> - HTML 使用标记标签来描述网页

**什么是XHTML?**
> XHTML 是更严谨更纯净的 HTML 版本。****
> - XHTML 指可扩展超文本标签语言（EXtensible HyperText Markup Language）。
> - XHTML 的目标是取代 HTML。
> - XHTML 与 HTML 4.01 几乎是相同的。
> - XHTML 是更严格更纯净的 HTML 版本。
> - XHTML 是作为一种 XML 应用被重新定义的 HTML。
> - XHTML 是一个 W3C 标准。

**HTML和XHTML的区别**
> - XHTML 元素必须被正确地嵌套。
> - XHTML 元素必须被关闭。
> - 标签名必须用小写字母。
> - XHTML 文档必须拥有根元素。

***

## Html的语义化

>语义化的HTML就是正确的标签做正确的事情，能够便于开发者阅读和写出更优雅的代码的同时让网络爬虫很好地解析。

- 1、为了在没有css代码时，也能呈现很好的内容结构，代码结构，以至于达到没有编程基础的非技术人员，也能看懂一二。（其实，就是为了不穿CSS外衣，裸奔依然好看）。

- 2、提高用户体验，比如：title，alt用于解释名词和图片信息。

- 3、利于SEO，语义化能和搜索引擎建立良好的联系，有利于爬虫抓取更多的有效信息。爬虫依赖于标签来确定上下文和各个关键字的权重。

- 4、方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）以语义的方式来渲染网页。

- 5、便于团队开发和维护，语义化更具可读性，如果遵循W3C标准的团队都遵循这个标准，可以减少差异化，利于规范化。

**Html语义化结构的注意点**

> h1~h6 ，作为标题使用，并且依据重要性递减，h1 是最高的等级

> 不要使用纯样式标签，如：b、font、u等，改用css设置

> 尽可能少的使用没有语义的div和span元素

> ul、ol、li，ul 无序列表

> dl、dt、dd，dl 就是“定义列表”

> 需要强调的文本，可以包含在strong或者em标签中（浏览器预设样式，能用CSS指定就不用他们），strong默认样式是加粗（不要用b，因为没语义），em是斜体（不用i同b）

> 在对语义要求不明显时，技能使用div也能使用p,那就使用p，以为p默认有上下边距，可以兼容特殊终端

> table、td、th、caption， (X)HTML中的表格不再是用来布局
使用表格时，标题要用caption，表头用thead，主体部分用tbody包围，尾部用tfoot包围。表头和一般单元格要区分开，表头标题用th，内容单元格用td；

***

## cookie、sessionSttorage、localStory区别

> `cookie`、`sessionSttorage`、`localStory`都是在客户端以键值对存储的存储机制，并且只能将值存储为字符串

| | cookie | localStorage | sessionStorage |
|:--------:|:--------:|:--------:|:--------:|
|由谁初始化|客户端或服务器，服务器可以使用Set-Cookie请求头。|客户端|客户端|
|过期时间|手动设置	|永不过期|当前页面关闭时|
|在当前浏览器会话（browser sessions）中是否保持不变|取决于是否设置了过期时间|是|否|
|是否与域名（domain）相关联|是|否|否|
|是否随着每个 HTTP 请求发送给服务器|是，Cookies 会通过Cookie请求头，自动发送给服务器|否|否|
|容量（每个域名）|4kb|5MB|5MB|
|访问权限|任意窗口|任意窗口|当前页面窗口|

**题目来源**
[来源链接](https://github.com/yangshun/front-end-interview-handbook/blob/master/Translations/Chinese/README.md)

**参考**
- [https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
- [http://tutorial.techaltum.com/local-and-session-storage.html](http://tutorial.techaltum.com/local-and-session-storage.html)

***

## Doctype的文档类型

**Doctype作用? 严格模式与混杂模式如何区分？有何意义？**
> - <!DOCTYPE> 声明必须是 HTML 文档的第一行，位于 <html> 标签之前.
> - <!DOCTYPE> 声明不是 HTML 标签；它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令。
> - 严格模式的排版和 JS 运作模式是 以该浏览器支持的最高标准运行。
> - DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现
> - 在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作。


**Doctype文档类型**
该标签可声明三种 DTD 类型，分别表示严格版本、过渡版本以及基于框架的 HTML 文档。

- HTML5 只有一种`<!DOCTYPE html>`
- HTML 4.01 规定了三种文档类型：Strict、Transitional 以及 Frameset。
- XHTML 1.0 规定了三种 XML 文档类型：Strict、Transitional 以及 Frameset。
- Standards （标准）模式（也就是严格呈现模式）用于呈现遵循最新标准的网页，而 Quirks
- （包容）模式（也就是松散呈现模式或者兼容模式）用于呈现为传统浏览器而设计的网页。

**知识点：HTML常用的 DOCTYPE 声明**
```
# HTML 5
<!DOCTYPE html>

# HTML 4.01 Strict
该 DTD 包含所有 HTML 元素和属性，但不包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

# HTML 4.01 Transitional
该 DTD 包含所有 HTML 元素和属性，包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">

# HTML 4.01 Frameset
该 DTD 等同于 HTML 4.01 Transitional，但允许框架集内容。
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"
"http://www.w3.org/TR/html4/frameset.dtd">
```
**知识点：XHTML常用的 DOCTYPE 声明**
```
# XHTML 1.0 Strict
该 DTD 包含所有 HTML 元素和属性，但不包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。必须以格式正确的 XML 来编写标记。
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

# XHTML 1.0 Transitional
该 DTD 包含所有 HTML 元素和属性，包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。必须以格式正确的 XML 来编写标记。
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "
http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

# XHTML 1.0 Frameset
该 DTD 等同于 XHTML 1.0 Transitional，但允许框架集内容.
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">

# XHTML 1.1
该 DTD 等同于 XHTML 1.0 Strict，但允许添加模型（例如提供对东亚语系的 ruby 支持）。
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
```