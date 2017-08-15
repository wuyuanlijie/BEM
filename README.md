# 你不知道的BEM！——实战篇
## 前言
一个好的CSS取名规则，可以让你的前端代码更容易理解和阅读，让你的代码复用性增强，项目更好的去
维护，BEM是你的一个选择!

## 首先了解什么是BEM命名规范
[BEM](http://en.bem.info/)相信大家都看过此类的文章，我就简单的聊聊吧，有些企业面试题就会问到这些...
BEM就是三个单词的缩写：Block（模块）、Element（元素）、Modifier（修饰符）。
1. Block一个独立的实体，代表了更高级别的组件（block）;
2. Element元素，抽象的说，就是block的后代，也就是子模块，用于形成一个完整的block整体（block__element）;
3. Modife修饰符，block与element上的标志，用于来表示形容他们的属性、状态、行为等等（block__--modifer）。

## 真理需要实践来检验

这里就有一个网页，但是我们可以发现他们的CSS样式很混乱，基本上就div+div+dib...这样的代码看起来让人很不舒服，
也很难去维护。所以我准备用BEM来规范它，仅供参考，不足的地方可以指出来！ <br><br>
首先我们贴出header部分，网页的头部包含了：`logo、menu、search、opts(写作与登录)` <br>
### 部分展示header的页面布局<br>
—>page <br>
——>page__hd <br>
———>page__logo <br>
———>page__menu <br>
—————>menu__item <br>
———>page__search  <br>
—————>search__form <br> 
————————>search__control <br>
———>page__opts

    
```html
<div class="page">
      <div class="page__hd">
        <div class="page__logo">
          <a href="/">
            <img src="http://7xpvay.com1.z0.glb.clouddn.com/logo.png">
          </a>
        </div>
        <ul class="page__menu">
            <li class="menu__item is-active">
              <a href="javascript:;"> 首 页 </a>
            </li>
            <li class="menu__item">
              <a href="javascript:;">热 门</a>
            </li>
            <li class="menu__item">
              <a href="javascript:;">关于我们</a>
            </li>
        </ul>
        <div class="text-right">
          <div class="page__search">
            <form action="/search" class="form search__form">
              <a href="javascript:;" class="icon">
                <img src="image/search.png" alt="">
              </a>
              <button type="button" name="button" class="btn">搜索</button>
              <input type="text" placeholder="搜索" class="search__control">
            </form>
          </div>
          <span class="page__opts">
            <a class="user" href="javascript:;">登录/注册</a>
            <a href="javascript:;">写作</a>
          </span>
        </div>
      </div>
</div>       
```
1. 相信有些人会问为什么meun的子元素是可以写成page__menu__item这样嘛？？？ <br>
答案：当然不行啊！如果这样使用的话，BEM就失去了它原有方便简洁性，反而更加增加代码的负担。 <br>
那么如何去嵌套组件？引用别人的话：`我们更倾向于组件的清单本身变为一个布局模块，并且清单子项目作为它的组件，使他们能够在其他地方独立使用`，
简单的说及就是就是创建一个新的组件模块，来摆脱重复的样式。menu__item就是这样出现的。
2. 为什么page__hd下面直接是page__logo?我们可以这样解释，因为在logo标签是独一无二的，我们就可以将层次减少，
在这里并没有一味的结构层次，而是经验层次！如果你使用多了，自然知道怎么去用。
### BEM实现的真实案例
1. [WeUI](https://weui.io/)这里面就是用BEM规范写的网页<br>
2. [BEM](http://en.bem.info/)网页

## BEM为什么我们要选择它?
可能对我们小白来说，我们去写几个比较小的网页，随便怎么去命名都无所谓，也就那么几个标签。
但是当你真正到了工作的时候，就是一个集体在工作，开发人员很多，每个人都有自己的一套命名，
这样会造成命名的识别度和一致性成为很大的问题，还会造成命名污染。<br>
### 那么BEM优势到底体现在哪里？
1. 第一点就是效率，就不如你管理班级，你可分成很多个小组，课代表收作业的时候，然后就可以安排组长去收，这样增加了效率，也不会让班级乱哄哄的去一窝蜂去交作业。
2. 第二点就是识别度高、结构清晰element 和 modifier 与 block 之间的从属关系，可以从名称上就一目了然的区分
3. 第三点就是命名的隔离性好，每一个区块之间都有是一个独立的空间，减少与其他元素的污染。
4. 第四点就是良好的扩展性，因为modifier修饰符的存在，当我们需要去添加按钮的样式的时候 只需要创建一个新的修饰符.btn--active{}
## 结束语

初学者看来，BEM看上去怪怪的，但是它的好处远远超过了它外面看上去的那些瑕疵。有点滑稽，而且会让我们输入更长的文本，但是它依然强大<br>
总之，BEM是一个非常有用，强大，简单的命名约定，以至于让你的前端代码更容易阅读和理解，更容易协作，更容易控制，更加健壮和明确而且更加严密。尽管你在开始的学习中会遇到一些问题，但是当你熟悉使用的时候，对我们前端开发者都是一个巨有价值的工具。


## 项目地址：
https://github.com/wuyuanlijie/gitbook_BEM

改写的网页有些地方不足，大家可以指出，谢谢！共同进步！

