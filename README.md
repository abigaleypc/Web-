# Web前端开发规范文档

主要针对前端最常见的HTML、CSS、JS实行规范开发，减少因为代码格式命名等问题引起的Bug。
我们的目标：不管有多少人共同参与同一项目，一定要确保每一行代码都像是同一个人编写的。

通用规范
-------
* Tab键用两个空格代替（Windows下TAB键占四个空格，Unix下TAB键占八个空格）。
* Css样式属性或者Js代码后加分号“;”    方便压缩工具“断句”。
* 文件内容编码均统一为UTF-8。
* Css、Js中的非注释类中文字符须转换成Unicode编码使用, 以避免编码错误时乱码显示。


HTML
-------
* html文件名以短横线(kebab-case)命名法，例如：user-profile.html
* 嵌套元素应当缩进一次（即4个空格）。<--- 这是唯一能保证在所有环境下获得一致展现的方法。
* 对于属性的定义，确保全部使用双引号，绝不要使用单引号。如<a href=""></a>

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
