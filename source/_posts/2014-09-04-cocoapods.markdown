---
layout: post
title: "CocoaPods"
date: 2014-09-04 15:53:50 +0800
keywords: iOS,CocoaPods,第三方库,Ruby,XCode
comments: true
categories: 
---
在做iOS项目开发时，大量的第三方库极大的提高了我们的开发效率。随着功能的不断增加，工程变得越来越庞大，使用到的第三方库也越来越多，这时第三方库管理工具CocoaPods的重要性就凸显出来了。在第三方库的引入、升级、依赖关系上，CocoaPods让一切变得简单。
1.安装
安装CocoaPods依赖Ruby环境
gem install cocoapods
2.使用
现在iOS开发中使用到的大部分第三方库都支持了CocoaPods，具体到使用的库时，我们可以查询下是否支持。
pod search EGOTableViewPullRefresh



在工程的主目录中创建文件Podfile，将工程中需要使用的库的名称及对应版本写到这个文件中。
pod 'EGOTableViewPullRefresh', '~> 0.1.0'

pod install
安装完成后，在工程的主目录中生成一个工程名对应的.xcworkspace文件，以后就使用这个文件来打开工程。
以后在需要往工程中添加第三方库时，先编辑Podfile文件，然后执行pod update.