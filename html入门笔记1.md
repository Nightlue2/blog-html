# 真·html入门笔记1

## 1.html是谁发明的
  Timothy John Berners-Lee，也称李爵士。作为万维网的发明者，一名计算机科学家，他创造了html这个超文本标记语言。

## 2.html起手写啥？
  起手式当然是用vscode打开工作目录，创建文件，按下 ! + tab 键啦！

  像<!DOCTYPE html>就是告诉浏览器当前文档所用的版本为html5，而<html lang="en">则是说对应语言为英文。

  head标签里面的东西都是不可见的，<meta charset="utf-8">是说文档的编码方式是utf-8，<meta name="viewport" content="width=device-width,initial-scale=1.0">是说该页面禁用缩放，且兼容手机，<meta http-equiv="X-UA-Compatible" content="ie=edge">则是说ie浏览器应使用最新的内核。


## 3.常用的表示章节的标签？
  按顺序来分：
  * header----总是显示在网页的最上面，可以包含logo、搜索框、标题元素。
  * article----表示文章的元素，可以嵌套使用，通常表示博客或者专栏的一些文章。
  * main----main元素的内容是独一无二的，logo、侧边栏、导航栏不应包含在其内。
  * section----如果元素内容可分几个部分，一般用article而不是section，不要把section当div用。
  * h1~h6----避免跳过某级标题，避免多h1标题，标签是为了语义化，为了seo，样式靠css。
  * p----表示段落的元素，align属性不推荐使用。
  * div----一般在无其他语义元素可用时才使用。
  * aside----可用于侧边栏或者标注框，内容独立于页面的主要内容。
  * footer----一般用于页面的页脚，不包含新的章节。

## 4.全局属性有哪些？
  class、style、id这些都是老生长谈的了，class可以用空格分隔值，而id只能有一个，且不同标签只能有一个id（id值不能包含空白字符），style还是一个标签。

  contenteditable用于控制元素是否可编辑，由于是枚举属性，所以要写是true还是false。hidden则是个布尔属性，用于隐藏一些页面属性直到满足某些条件。tabindex属性接受一个整数，顺序为从正值、0到非法值，负值不可以被导向。title属性在mdn上的解释非常令人费解，其作用其实是当你鼠标移到该元素上的时候显示你想显示的东西。

## 5.常用的表示内容的标签？
  * ol+li----ordered list和list item的简称，可嵌套，start=8和type='I'这两个属性需要了解。
  * ul+li----unordered list和list item的简称，可嵌套，只有全局属性。可用list-style-type加以修饰。
  * dl+dt+dd----description list和description term和description data的简称，dt和dd是可以多对多的，整体是一个键值对表，dt只包含全局属性。
  * pre----以等宽字体的形式展示元素中的文本，包括空格和换行符。
  * hr----一条水平分割线，语义上的而非表现层面上的。
  * br----使文本产生回车。
  * a----锚元素，创建超链接，具有多种属性，太多省略。
  * em----标记用户需要着重阅读的内容，一般显示为斜体，强调语义。
  * strong----标记文本十分重要，一般显示为粗体，比em要更加强调。
  * code----用来写代码的，显示为等宽字体。
  * quote----行内引用元素，会有引号显示出来。
  * blockquote----块级引用元素，会有一定量的缩进，可以通过css修改。
