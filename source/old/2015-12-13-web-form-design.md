---
layout:     post
title:      Web表单设计的艺术
excerpt: 我所在的公司是为健身房提供管理系统的，这样的管理系统经常涉及到大量的表单填写，可能对于大多数人来说，表单看起来都差不多，但接触到真正的设计工作时，才发现要设计出交互简单而自然的表单并不简单，表单中标签的对齐方式、内容的归类方式、出错提示等都应该是经过仔细考量的...

category:	UI/UX

tags:
  - Blog
---

我所在的公司是为健身房提供管理系统的，这样的管理系统经常涉及到大量的表单填写，可能对于大多数人来说，表单看起来都差不多，但接触到真正的设计工作时，才发现要设计出交互简单而自然的表单并不简单，表单中标签的对齐方式、内容的归类方式、出错提示等都应该是经过仔细考量的。

最近抽空通读了「WEB表单设计——点石成金的艺术」，里面关于表单的排版和交互原则浅显易懂，在平时的设计工作中也都会用到，趁着记忆还鲜活，整理了一份读书笔记，列出了平时常见的需要注意的点，附一份思维脑图。[查看大图](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/WEBform.png)

![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/WEBform.png)

## 表单结构

> 虽然很多视觉设计和交互设计考虑因素对完成表单填写都发挥着重要作用，但真正起作用的通常是表单的内容及组织方式。

在界面设计中，内容始终都是第一要素，界面中的视觉元素最终都是服务于内容的。因此在设计表单之初，应当选取表单问题，决定什么问题可以留在表单中：保留完成表单必须的问题，删减不必要的问题，不必立刻回答的问题可以留到以后再问，对用户可能不熟悉、产生不信任的问题进行解释。我们的目标是使用户尽快填完表单，每多一个不必要的问题，用户离开的几率也多一分。

根据问题的数量和情境，可以将问题分成若干个有意义的组，但是内容组之间不需要使用大量的视觉差异，使用最少的视觉信息有助于保持焦点在内容上，而不是表现形式，无意义的视觉元素其实很可能是个累赘。

> 信息由产生作用的差异构成。—— Edward Tufte

此外，应当为表单提供清晰的填写路径，可以大大提高填写速度。
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/%E6%B8%85%E6%99%B0%E7%9A%84%E8%B7%AF%E5%BE%84.png)

需要注意的是，应当避免使用进程指示，或者使用笼统的、没有明确设置期望值的进程指示，因为有时进程指示会错误显示完成表单所需的网页页数和步骤，例如在选择收货地址时，倘若列表中没有要选择的地址，则需要跳出进程，从而一步变成了两步。

## 表单元素

#### 1.标签
标签应当采用用户能明白的语言，尽量简洁，同时表单元素的布局也影响着用户完成表单。根据标签的对齐方式可以分为以下几种。

▼ 顶对齐标签：完成路径很清晰，是完成表单最快捷的布局方式，且水平方向可以自由组合多个问题，但会占用额外的垂直空间。
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/%E9%A1%B6%E5%AF%B9%E9%BD%90%E6%A0%87%E7%AD%BE.png)

▼ 右对齐标签：也比较快捷，标签和输入框距离较近，容易处理，但由于标签左侧不齐，会降低浏览效率，因此比较适用于填写常见问题的情况，另外标签的长度也容易产生灵活性问题。
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/%E5%8F%B3%E5%AF%B9%E9%BD%90%E6%A0%87%E7%AD%BE.png)

▼ 左对齐标签：表单问题的可读性较强，适用于填写不熟悉的问题的情况，但由于标签长度的不确定性可能导致标签和输入框的距离增加，使得关联性变弱，减慢完成表单的速度，同时也存在灵活性问题。
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/%E5%B7%A6%E5%AF%B9%E9%BD%90%E6%A0%87%E7%AD%BE.png)

▼ 输入框内的标签：减少所需的屏幕空间，但一旦填写后就找不到问题，因此不适用于表单较长的情况，另外需要注意的是，应当区分开标签和实际答案。
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/%E8%BE%93%E5%85%A5%E6%A1%86%E5%86%85%E7%9A%84%E6%A0%87%E7%AD%BE.png)

#### 2.输入框
应当根据问题的答案选择合适的输入框类型，例如是用文本输入框还是用单选框或者下拉菜单。

如果采用文本输入框，输入框的长度应当为用户提供暗示，例如填写电话号码和邮政编码的输入框，这两者的答案的长度都是固定的，如果采用和其他问题一样长度的输入框，有可能会让用户产生疑惑。

对于表单中的必填项，应当明确标识出来，但如果必填项占大多数，可以选择把可选项标识出来。

#### 3.动作
表单中的主动作是完成表单的最主要行为，如提交、保存、继续等，次动作则是与主动作相悖的动作，如取消、重置、返回等，在视觉上应当区分主动作和次动作，如按钮和链接组合、不同颜色的按钮等。
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/%E5%8A%A8%E4%BD%9C.png)

完成表单的过程中，即使主动作不可用，也要总是可见，视觉上是不可点击的即可；点击主动作后，应当给予反馈，防止多次重复提交。

## 表单的交互

#### 1.验证
在填写表单的过程中，应当对用户的答案进行即时验证，而不要等到填写完成点击提交按钮时再进行验证。

确认：适用于错误率高或者有特定格式要求的问题，例如电话号码，明确是11位数字；

建议：有些问题，可以为用户提供回答建议，确保用户提供有效答案，例如新浪微博中填写用户昵称时，当名字已被占用时，系统会建议其他名字；

限制：有些问题没有明确定义的答案，但有明确定义的限制，例如很多网站为了增强用户密码的安全性，建议用户设置同时含有字母、数字和符号的密码。

#### 2.帮助
对于用户不熟悉的问题，系统应该提供帮助，但应当尽量减少表单中的帮助文字，文字过多会分散用户的注意力，且用户一般不会去仔细阅读帮助文字，因此帮助文字应当尽量简洁清晰，且出现在用户需要的地方。下面以新浪微博中的帮助为例说明几种主要的帮助形式。

▼ 自动即时帮助：在最合适的时间和位置显示帮助信息，但只有在开始填表时，用户才知道是否有帮助文字。
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/%E5%8D%B3%E6%97%B6%E5%B8%AE%E5%8A%A9.png)

▼ 输入框内的hint提示文字：优化了自动即时帮助的缺点，但帮助信息的长度受到限制。
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/hint.png)

▼ 用户激活的即时帮助
![image](https://github.com/CloverTuan/Markdown_Images/raw/master/web-form-design/%E6%BF%80%E6%B4%BB%E7%9A%84%E5%B8%AE%E5%8A%A9.png)

#### 3.错误与成功
如果有错误阻碍用户完成表单，应当明确告诉用户，错误消息确保以最重要的形式表现，以便快速解决；如果表单填写成功，应当用成功消息清晰传达，并显示结果，但不要让成功消息阻止进程，应当明确告诉用户下一步做什么。

## 写在最后

设计原则是任何一种解决方案的指路灯，设计模式是解决情境问题的实际方案，在实际的设计工作中，还应当结合问题的实际情况，合适的、能完美解决问题的就是最好的。