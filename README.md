# Web前端开发规范文档

主要针对前端最常见的HTML、CSS、JS实行规范开发，减少因为代码格式命名等问题引起的Bug。
我们的目标：不管有多少人共同参与同一项目，一定要确保每一行代码都像是同一个人编写的。

通用规范
-------
1. Tab键用两个空格代替（Windows下TAB键占四个空格，Unix下TAB键占八个空格）。
2. Css样式属性或者Js代码后加分号“;”    方便压缩工具“断句”。
3. 文件内容编码均统一为UTF-8。
4. Css、Js中的非注释类中文字符须转换成Unicode编码使用, 以避免编码错误时乱码显示。


HTML
-------
1. html文件名以短横线(kebab-case)命名法，例如：user-profile.html
2. 嵌套元素应当缩进一次（即4个空格）。
3. 对于属性的定义，确保全部使用双引号，绝不要使用单引号。如 ```<a href=""></a>```
4. 尽量避免多余的父元素
```html
<!-- 不好 -->
<span class="avatar">
  <img src="...">
</span>

<!-- 好 -->
<img class="avatar" src="...">
```

html模板如下：
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=Edge">
    <title>Page title</title>
  </head>
  <body>
    <img src="images/company-logo.png" alt="Company">
    <h1 class="hello-world">Hello, world!</h1>
  </body>
</html>
```


CSS
-------
1. 选择器中的属性添加双引号，例如，```input[type="text"]```
2. 每个声明块的左花括号前添加一个空格
3. 每条声明都应该独占一行,以分号结尾
4. 使用简写形式的十六进制值，例如，用 #fff 代替 #ffffff
5. 避免为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px;
6. 避免使用!important
7. class名称短横线(kebab-case)命名法,只能出现小写字母和短横线
8. 使用有意义的类名。使用有组织的或目的明确的名称，不要使用表现形式（presentational）的名称
9. 基于最近的父 class 或基本（base） class 作为新 class 的前缀
10. 避免使用属性选择器（例如，```[class^="..."]```）
11. 相关功能的样式放在一块，多个功能块之间用空白块分隔，并加以注释说明此块的作用

示例：
```css
/* Bad CSS */
.selector, .selector-secondary, .selector[type=text] {
  padding:15px;
  margin:0px 0px 15px;
  background-color:rgba(0, 0, 0, 0.5);
  box-shadow:0px 1px 2px #CCC,inset 0 1px 0 #FFFFFF
}

/* Good CSS */
.selector,
.selector-secondary,
.selector[type="text"] {
  padding: 15px;
  margin-bottom: 15px;
  background-color: rgba(0,0,0,.5);
  box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #fff;
}
```









