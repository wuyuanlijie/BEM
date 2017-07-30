# 你不知道的BEM！——实践篇
## 前言
一个好的CSS取名规则，可以让你的前端代码更容易理解和阅读，让你的代码复用性增强，项目更好的去
维护，BEM是你的一个选择!

## 首先了解什么是BEM命名规范
[BEM](http://en.bem.info/)相信大家都看过此类的文章，我就简单的聊聊吧，有些企业面试题就会问到这些...
BEM就是三个单词的缩写：Block（模块）、Element（元素）、Modifier（修饰符）。
1. Block一个独立的实体，代表了更高级别的组件（block）;
2. Element元素，抽象的说，就是block的后代，也就是子模块，用于形成一个完整的block整体（block__element）;
3. Modife修饰符，block与element上的标志，用于来表示形容他们的属性、状态、行为等等（block__element--modifer）。

## 
