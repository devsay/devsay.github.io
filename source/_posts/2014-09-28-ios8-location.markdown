---
layout: post
title: "ios8 定位服务"
date: 2014-09-28 21:50:25 +0800
keywords: iOS8,XCode6,CLLocationManager,定位服务
comments: true
categories: 
---
笔者将XCode5升级到Xcode6，iOS7升级到iOS8，重新编译发现工程无法使用定位服务，App启动时也没提示用户是否允许当前App使用定位服务。

iOS8对定位服务做了修改，需要在info.plist增加一项：
NSLocationWhenInUseUsageDescription 这里可以自定义对用户的提示。
重新编译时，系统就会提示用户是否允许App启用定位服务。

今天先这样，明天深入研究下。