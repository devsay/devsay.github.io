---
layout: post
title: "Sizeclass"
date: 2014-10-22 19:52:03 +0800
comments: true
keywords: sizeclass, autolayout, 约束, 自动布局, xib
categories: 
---

1.Size Class:

Size Classes是iOS8中提出的新概念，表示对所有iOS设备的一个抽象，每个组合对应了不同的设备分类。

XCode6默认新创建的Xib是一个正方形，Size Class默认的值是wAny | hAny，对应所有iOS设备的layout。

![](/images/sizeclass/0.png)

横向即Width的取值依次为: Compact Any Regular

纵向即Height的取值依次为：Compact Any Regular
两者共可搭配出9中layout。


2.约束：

Autolayout的核心是约束。

可以点击XCode的Editor菜单添加约束项，但每次只能选择一个。

![](/images/sizeclass/1.png)

还可以点击右下角的一排按钮，可以同时添加或修改多个约束项，非常方便。

![](/images/sizeclass/2.png)

其中有些约束是针对多个UIView的，你需要同时选中多个UIView才能添加。

![](/images/sizeclass/3.png)

添加约束的关键是让系统能够根据你添加的约束确定视图的准确位置，如果添加的约束过少或者互相矛盾就会报错。

![](/images/sizeclass/4.png)