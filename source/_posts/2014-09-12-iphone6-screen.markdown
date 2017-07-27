---
layout: post
title: "iPhone6分辨率适配"
date: 2014-09-12 15:51:29 +0800
keywords: iOS,iPhone6,屏幕,适配,ppi,光栅化,分辨率
comments: true
categories: 
---

9月10日苹果正式发布了全新的iPhone6、iPhone6 Plus, 相比之前, 这次iPhone在屏幕尺寸上变化巨大。最近开发者和设计师们都很关心自己的App应该怎么来对两款iPhone6适配。

先看苹果历代iPhone公布的分辨率及ppi
iPhone6 Plus: 1920x1080, 401 ppi
iPhone6: 1334x750, 326 ppi
iPhone5s: 1136x640, 326 ppi
iPhone4：960x640, 326 ppi

iPhone6与iPhone4，iPhone5s的ppi是一样的


iPhone6 Plus准确尺寸: 1242x2208

Points做iOS开发时, 我们使用的是Points, 系统会将Points整数倍处理光栅化为Rendered Pixels, 再将Rendered Pixel转换成Physical Pixels在屏幕上显示出来。
320x480点坐标系经过2x渲染之后的Rendered Pixels为640x960
iPhone6: 375x667点坐标系经过2x渲染之后的Rendered Pixels为750x1334
iPhone6 Plus: 414x736点坐标系进过3x渲染之后的Rendered Pixel为1242x2208
但是iPhone6 Plus实际分辨率为1080x1920，在Rendered Pixel会进行降低采样率的处理来显示在物理设备上。
