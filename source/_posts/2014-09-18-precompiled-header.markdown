---
layout: post
title: "fatal error: file has been modified since the precompiled header"
date: 2014-09-18 10:20:28 +0800
keywords: iOS,precompiled header,has been modified,DeriveData,XCode
comments: true
categories: 
---

编译工程时，报错

fatal error: file '/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/ iPhoneOS8.0.sdk/System/Library/Frameworks/AVFoundation.framework/Headers/AVAudioSession.h' has been modified since the precompiled header '/Users/Mac/Library/Developer/Xcode/DerivedData/xxx-frlhxpamlowshtayyttcuivhpzcw/Build/Intermediates/PrecompiledHeaders/xxx-Prefix-Debug-dmssclbwyzjgywetcgfenqhmlpdi/xxx-Prefix-Debug.pch.pch' was built

xxx表示工程名称

仔细查找原因，发现是不小心改动了AVAudioSession.h这个头文件导致的

解决办法：

1.Product->Clean

2.删除~/Library/Developer/Xcode/DeriveData/下所有文件

重新编译，成功。