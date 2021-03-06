---
title: 分布式社交展望
template: default
---

name: inverse
layout: true
class: center, middle, inverse

---

# 分布式社交展望
王子博
.footnote[[源文件](https://github.com/Smart-Hypercube/sfd2017) [幻灯片](http://0x01.me/sfd2017) [寻找存档](https://lug.ustc.edu.cn/)]
???
上世纪60年代，出于冷战的考虑，美国认识到在不同的计算机系统、不同的局部网络之间建立可靠的连接是非常重要的。在这个想法下，ARPA网应运而生。ARPA被创造者们最津津乐道的特性之一就是它用到了分散网络技术，将所有网络节点连接成了分布式的网络，这使得它的可靠性远高于中心化的网络。

---

layout: false
.left-column[
## 发展
]
.right-column[
### ARPA网

### 互联网

### 万维网

### 电子邮件
]
???
继承着这样的思想，有了后来的互联网，又有了其上的万维网和电子邮件系统。这些系统都有一个特点，就是每个人的内容和服务被分布于整个网络的各个角落，大家通过一致的接口互相访问和对接。因此，网络非常健全，任何野心家都不能控制整个网络，任何单点事故都不会摧毁整个网络。可以说，分布式是互联网发展的重要支柱之一。

---

.left-column[
## 发展
## 实现
]
.right-column[
### 统一标识
- URI
- 电子邮件地址

### 统一接口
- HTTP
- SMTP

### 单向对接
- 超链接
- 信封地址
]
???
刚刚提到了万维网和电子邮件系统，我非常喜欢它们的一些设计。当时，为了能让完全不同的机器、软件和用户进行对接，互联网先驱们设计了伟大的架构，这架构由三大核心思想构成：统一标识、统一接口、单向对接。

---

.left-column[
## 发展
## 实现
## 实践
]
.right-column[
### 独立博客
使用URL或域名作为统一标识

使用HTTP、HTML、RSS/Atom等接口对接

使用友链关联
]
???
曾经的先驱们更多受到不得不融合完全不同的机器和软件的困扰。今天，我们虽然已经能成功的将机器连接在一起，却被种种人为设置的困难，通常是服务提供商为了绑住用户，挡在统一、标准和开放的门外。

---

.left-column[
## 发展
## 实现
## 实践
## 如今？
]
.right-column[
### 界面可定制性低

### 支持的内容形式少
- 无法图文混排
- 无法评论带图

### 难以存档、过滤、搜索

### 只能与同平台用户交互

### 内容审查横行
- 政治审查
- 商业竞争
]
???
xkcd是一个典型的博主需求例子，它的界面简洁而统一，虽然一般都只是图片，但时常有特殊的漫画。

---

template: inverse
## 即时聊天
![xkcd:1810](https://imgs.xkcd.com/comics/chat_systems.png)
???
这是封闭性的重灾区，为什么我们不能像邮件那样和想联系的人联系呢？

---

.left-column[
## 邮件
]
.right-column[
### 优势
- 可跨域交流
- 服务商和应用程序丰富
- 易于自动化处理
- 群发方便
- 支持多线索讨论
- 自带多分支历史记录
- 可签名或加密

### 劣势
- 实时性差
- 讨论串变长时内容迅速增大
]

---

.left-column[
## 邮件
## XMPP
]
.right-column[
原名Jabber

### 优势
- 可跨域交流
- 基于XML
- 实时性好
- 原生支持点对点加密

### 劣势
- 服务商和应用程序少
]

---

.left-column[
## 邮件
## XMPP
## IRC
]
.right-column[
### 优势
- 群聊方便

### 劣势
- 只能群聊……
]

---

.left-column[
## 邮件
## XMPP
## IRC
## 实践
]
.right-column[
[\*@0x01.me](mailto:hypercube@0x01.me)
]

---

template: inverse
## 社交网络
朋友圈
QQ空间
微博
Facebook
Twitter
Instagram
微信公众号
……
???
我们真的需要这么多向世界发布消息的平台吗？

---

.left-column[
## 博客
]
.right-column[
*微博*的本意就是*微型博客*

### 优势
- 独立自由
- 易于个性化
- 可与电子邮件或RSS/Atom整合实现订阅

### 劣势
- 不易管理权限
- 不易机读和整合
]

---

.left-column[
## 博客
## OStatus
]
.right-column[
一种动态更新协议

### 优势
- 可跨域交流
- 可选择服务商和应用程序

### 劣势
- 需要服务商
- 不易定制
]
???
GNU social就是一个支持OStatus接口的开源社交服务器程序，它还支持Twitter接口，以及允许用户通过XMPP发布微博。

---

.left-column[
## 博客
## OStatus
## 邮件
]
.right-column[
### 优势
- 可跨域交流
- 服务商和应用程序丰富
- 可定制性较好
- 易于机读、存档、过滤

### 劣势
- 对大公众号不适用
]
???
GNU social就是一个支持OStatus接口的开源社交服务器程序，它还支持Twitter接口，以及允许用户通过XMPP发布微博。

---

.left-column[
## 博客
## OStatus
## 邮件
## 实践
]
.right-column[
[feed.0x01.me](http://feed.0x01.me/)
]

---

template: inverse
## 日程表
???
如果大家都接入同一个日程管理系统，会有巨大的方便，如公司内所有事项都通过日程邀请来实现，也可以互相查看别人的日程来决定约会时间，以及通过Busy/Available指示了解对方状态。

很久以前QQ有过状态指示器，现在没人用了，为什么？因为没人喜欢额外设置这个，应当自动生成。

应用场景：教师向大家分享课程时间、朋友约活动、社团办活动。

---

.left-column[
## iCal
]
.right-column[
一种开放日程表格式

### 问题
- 不方便订阅
- 支持的字段不够丰富，不易扩展
]
???
每次要下载全部更新，或许可以设置一个时间戳机制？

---

.left-column[
## iCal
## 实践
]
.right-column[
使用Google Calendar管理日程

以HTML发布在[status.0x01.me](http://status.0x01.me/)

![status.0x01.me](/status.png)

Google还支持提供iCal格式，以及某种状态更新接口
]

---

template: inverse
## 渐进过渡与整合
???
唯一可行的方式：先用各种机器人，如IFTTT对接起来，用户量大了后，有了需求，服务商就会愿意接入。

希望大家都能试一试，开始使用，我们将会得到更加开放和自由的互联网

---

template: inverse
## 谢谢大家












