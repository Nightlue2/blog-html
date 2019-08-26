# html入门笔记2

## a标签用法

  href="#" 或 href="" 或 href="javascript:;"
  以上是简写，第一个是回到页面顶部，第二个是刷新页面，第三个则是什么都不做（伪协议）。

  href="//google.com"
  老师推荐的最优写法，非文件协议，不管是http还是https都可以访问。

  href="#id名"
  可以定位到id选择器名字所在元素处。

  href="mailto:conhttp@163.com"
  港真，没啥用，win10会询问用啥来打开，然而自带的邮箱咱一般不用，chrome也不能打开，还不如用一个不能打开的展示文本来show your email。

  href="tel:+86 13411112222"
  也没啥用，win10还是会让你选取应用打开。

  href="2.jpg" download="美女.jpg"
  用来下载文件，后面的是下载下来的文件名。不设置的话就默认名字。手机浏览器可能不支持这种方式。

    <a href="//baidu.com" target="_self">
  
  用于指示浏览器在何处打开资源，像self就是说在当前页面加载，如果是_blank的话就是新窗口，如果有iframe的话，那么_parent就是在父框架打开，_top就是在顶层打开。假如有a窗口，target="a"就是说在a窗口打开。

    <a href="//baidu.com" target="_blank" rel=noopener>
  
  用于防止新开页面利用其属性值控制前一个页面，旧浏览器还有个noreferrer的值，新的可以不加这个值。

## table标签用法
```html
  <table>
    <thead><tr><th></th></tr></thead>
    <tbody><tr><td></td></tr></tbody>
    <tfoot><tr><td></td></tr></tfoot>
  </table>
```
  一般来说，比较标准的写法就是把thead和tbody和tfoot都写上，tr代表table row，td则代表table data。
```html
  <style>
    table{
      table-layout:fixed/auto...;
      border-collapse:collapse;
      border-spacing:none;
    }
  </style>
```
  这个第一句就是告诉浏览器如何布局表格，第二句是使表格的各项边框合并，第三句是在第二句没有写的情况下设置各单元格的边框距离。

## img标签用法

    <img src="dog.jpg" alt="一只狗子" width=100px>
  src属性当然是指明图片的链接了，height和width不能同时设置（底线），最好的方法是在img样式里面加个max-width:100%;这样就能完美适配移动端（响应式）
  
  id名.onload = function(){
    ...
  };
  js里面有个onload和onerror的事件，如果加载图片成功或者失败，那么就可以在控制台打印一些信息，或者显示其他诸如404的图片之类的操作。

  
