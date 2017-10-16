# Web前端开发规范文档

主要针对前端HTML、CSS、JS实行规范开发，统一代码格式，规范开发方法，减小项目维护成本

通用规范
-------
* Tab键用两个空格代替（Windows下Tab键占四个空格，Unix下Tab键占八个空格）。
* Css样式属性或者Js代码后加分号“;”    方便压缩工具“断句”。
* 文件内容编码均统一为UTF-8。
* Css、Js中的非注释类中文字符须转换成Unicode编码使用, 以避免编码错误时乱码显示。
* 文件名以短横线(kebab-case)命名法，例如：user-profile.html  、 loading-spinner.css 、 avatar-def.jpg


HTML
-------
* 嵌套元素应当缩进一次（即4个空格）。
* 对于属性的定义，确保全部使用双引号，绝不要使用单引号。如 ```<a href=""></a>```
* 尽量避免多余的父元素
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
* 选择器中的属性添加双引号，例如，```input[type="text"]```
* 每个声明块的左花括号前添加一个空格
* 每条声明都应该独占一行,以分号结尾
* 使用简写形式的十六进制值，例如，用 #fff 代替 #ffffff
* 避免为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px;
* class名称短横线(kebab-case)命名法,只能出现小写字母和短横线
* 使用有意义的类名。使用有组织的或目的明确的名称，不要使用表现形式（presentational）的名称
* 基于最近的父 class 或基本（base） class 作为新 class 的前缀
* 避免使用属性选择器（例如，```[class^="..."]```）
* 避免使用float属性
* 相关功能的样式放在一块，多个功能块之间用空白块分隔，并加以注释说明此块的作用
* 兼容多个浏览器时，将标准属性写在底部。如：
```css
-moz-border-radius: 15px; /* Firefox */
-webkit-border-radius: 15px; /* Safari和Chrome */
border-radius: 15px; /* Opera 10.5+, 以及使用了IE-CSS3的IE浏览器 *//标准属性
```
6个不要
* 不要在标签上直接写样式
* 不要在CSS中使用expression
* 不要在CSS中使用@import
* 不要在CSS中使用!important
* 不要在CSS中使用“*”选择符
* 不要将CSS样式写为单行

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

JS
-------
* 常量名使用单词大写加下划线，如: USER_NAME
* 变量、方法名以小驼峰，如：``` function getUserInfo (){}  let userProfile = ''; ```
* 构造器方法首字母大写，如：DefaultConfig
* 语句结束添加分号结束“;”
* 使用严格的条件判断符。用===代替==，用!==代替!=，避免掉入==造成的陷阱
在条件判断时，这样的一些值表示false
```javascript 
null
undefined与null相等
字符串''
数字0
NaN
```




VUE
-------








