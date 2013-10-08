Campus Pipe
===========


Campus Pipe 是一个基于 Meteor 开发的校园生活应用网站。
--------------------------------------------------------------------------------------

  1. [Campus Pipe] 是一个匿名信息推送或交换平台，目前主要针对 *校园交友及校际联谊* 提供信息传递功能。

  2. [Meteor] is an open-source platform for building top-quality web apps in a fraction of the time, whether you're an expert developer or just getting started.

  3. 校园生活应用网站，即面向在校学生的本地化信息服务网站。


> 初衷是消暑，打发无聊的假期。从上学期末着手准备，断断续续地进行着，一边天马行空突发奇想地找点子，另一边循规蹈矩不厌其烦地debug。到现在有三个月了，整个项目也渐具雏形，但是离发布还有一定距离。作为本项目的发起者兼唯一开发人员（至少目前为止）， **我希望有更多的小伙伴加入 Campus Pipe =)**


Campus Pipe 的初步设想
------------------------------------

### 从 [瀚海星云] 说起

经常在科大BBS逗留的同学必定对 [PieBridge] （俗称pie板）不陌生，上面的征友信息五花八门。偶有美女出没，便引得无数科男折腰垂涎（我也打过酱油捧过场--）。但是，仔细一看，征友者多为校外人士，难道在校生就没有需求？实际上，众人皆知，寂寞的大多数（在校生）似乎永远在骚动，却毫无行动。为什么呢？发帖可能意味着需要公开个人信息，甚至是私密照片。消息一传开，便成众人谈资，特别是还要被好朋友逮住盘问一番。在这种舆论环境下， **公开征友** 要很大的勇气，也意味着沉重的心理压力。

### 公开征友的匿名模式

之前与女朋友讨论过此类问题，我说，在无需承担任何压力（包括社会舆论或道德规范等所施加的）的情况下，身边那些单身的同学会选择上 BBS 公开征友么？ 她没有回答，却反问道：怎么可能会没有任何外界压力呢？
确实如此，在现实生活中，压力无处不在。但是，不可否认的是，有办法可以缓解部分压力，甚至可以就事论事有针对性地排除主要压力。

言归正传，公开征友的过程中会遇到很多压力，主要是心理上的。其中最害怕的是，个人信息公开后会引来同学们的过分关注，招致众多无关人士的评头论足。其次是如何面对那些应征对象，庞大的应征队伍不仅耗费时间，也会遇到各种奇葩或熟人，私下交换照片特别是会面都挺尴尬的。此二者乃重中之重，其它皆为琐碎之事。

解决上述问题，最简单的方法，我想就是传小纸条（小学生必备，不要被老师发现哦==）。不过，这只局限于方圆百步之内。设想一下，如果有一个专门管道用来传小纸条，而收信者对其却来源毫不知情。就像《[1984]》中所叙述的一样， *这气动管最后通向个看不见的迷宫*。

### 使用 Campus Pipe 传送小纸条

具体技术实现过程中，我们为每张小纸条配备许多根私密的传递管，以保证传送人与各个接收者之间的独立私密性。发小纸条的时候可以设置传送目的地或目标，也可以屏蔽掉部分人群，当然，收信者也可以拒绝接收。需要注意的是，不要在小纸条上透露个人信息，也不能撰写虚假或无效信息。

**那么，该如何保证信息的有效性及发送者的真实存在性？**

发送者的真实存在性是信息有效性的基础，为了保证真实存在，我们采用 **校园邮箱** 注册，并且需要输入 **学号**，这些 **都不公开**。信息的有效性则需要收信者来甄别，通过举报来投诉不良行为，对于不良行为或虚假信息，采取"零容忍"原则。

另外，为了方便交换照片，开发了相关应用以保证交换的公正性，两人在线同步交换，在遇到欺骗行为时，可立即撤回相片并举报对方。

Campus Pipe in practice
-----------------------------------

### Tech. requirements
  + Languages
    - JavaScript, or **[CoffeeScript]** (preferred)
    - CSS, or **[Stylus]** (preferred)
    - HTML and Templates (Mustache, [Handlebars] etc.)
  + frameworks (and JS libs)
    - [Node.js]
    - [Meteor] and its packages (including [smart packages](https://atmosphere.meteor.com/))
    - [MongoDB] (default database) JavaScript driver
    - **[Bootstrap]** 3.x
    - **[jQuery]** and [Underscore.js]
  + programming
    - OS: any, I'm working on [Linux Mint].
    - Editor: **VI** (preferred)
    - browser supported: IE 8+ and other mordern browsers

### Design Overview

```
Campus Pipe ---+--- app: pipe     ---  Send and receive pipe message
               |
               +--- app: gossip   ---  Anonymously real-time chat
               |
               +--- app: register ---  Campus based registration
```

### Code Sources

  1. ```git clone https://gitgeek.net/rug/campus-pipe.git```

  2. home page: http://gitlab.lug.ustc.edu.cn/rug/campus-pipe

  3. website demo: http://pipe.meteor.com/ (test on chrome only)

  4. [@wulx](https://github.com/wulx) and [blog](http://rug.blog.ustc.edu.cn/)


*Free Software, Hell Yeah!*

  [Meteor]: http://www.meteor.com/  "an ultra-simple, database-everywhere, data-on-the-wire, pure-Javascript web framework"
  [Campus Pipe]: http://pipe.meteor.com/  "Campus Pipe, made with Meteor"
  [瀚海星云]: http://bbs.ustc.edu.cn/  "瀚海星云 BBS@USTC"
  [PieBridge]: http://bbs.ustc.edu.cn/cgi/bbstdoc?board=PieBridge  "瀚海星云 PieBridge讨论区"
  [1984]: http://book.douban.com/subject/5299764/  "《1984》, 乔治· 奥威尔"
  [CoffeeScript]: http://coffeescript.org/  "a little language that compiles into JavaScript"
  [Stylus]: http://learnboost.github.io/stylus/  "Expressive, dynamic, robust CSS"
  [Handlebars]: http://handlebarsjs.com/  "build semantic templates effectively with no frustration"
  [MongoDB]: http://www.mongodb.org/  "an open-source document database, and the leading NoSQL database"
  [Node.js]: http://nodejs.org/ "evented I/O for v8 javascript"
  [Bootstrap]: http://twbs.github.io/bootstrap/  "Sleek, intuitive, and powerful mobile first front-end framework for faster and easier web development"
  [jQuery]: http://jquery.com/  "a fast, small, and feature-rich JavaScript library"
  [Underscore.js]: http://underscorejs.org/  "JavaScript's utility _ belt"
  [Linux Mint]: http://www.linuxmint.com/  "a modern, elegant and comfortable operating system"
  
