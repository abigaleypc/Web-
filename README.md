# Web前端开发规范文档

主要针对前端最常见的HTML、CSS、JS实行规范开发，减少因为代码格式命名等问题引起的Bug。
我们的目标：不管有多少人共同参与同一项目，一定要确保每一行代码都像是同一个人编写的。

通用规范
-------
*Tab键用两个空格代替（Windows下TAB键占四个空格，Unix下TAB键占八个空格）。
*Css样式属性或者Js代码后加分号“;”    方便压缩工具“断句”。
*文件内容编码均统一为UTF-8。
*Css、Js中的非注释类中文字符须转换成Unicode编码使用, 以避免编码错误时乱码显示。

文件规范
-------
*文件名用英文单词，多个单词用驼峰命名法。
*一些浏览器会将含有这些词的作为广告拦截，文件命名、ID、CLASS等所有命名避免以上词汇。
`ad`、`ads`、`adv`、`banner`、`sponsor`、`gg`、`guangg`、`guanggao`等


HTML
-------

*用两个空格来代替制表符（tab） <--- 这是唯一能保证在所有环境下获得一致展现的方法。
*嵌套元素应当缩进一次（即两个空格）。
*对于属性的定义，确保全部使用双引号，绝不要使用单引号。如<a href=""></a>

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Page title</title>
  </head>
  <body>
    <img src="images/company-logo.png" alt="Company">
    <h1 class="hello-world">Hello, world!</h1>
  </body>
</html>
```
