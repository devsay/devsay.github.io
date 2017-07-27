---
layout: post
title: "ios定位服务CoreLocation"
date: 2014-10-10 19:22:23 +0800
comments: true
categories: 
---

基于LBS的应用开发是当今移动开发中的一大热门, 其中主要涉及到地图和定位两个方面.

iOS开发中, 定位服务依赖于CoreLocation框架, CLLocationManager是CoreLocation中的核心类.

初始化:

if ([CLLocationManagerlocationServicesEnabled]) {
            self.locationManager = [[CLLocationManageralloc]init];
            self.locationManager.delegate =self;
            self.locationManager.desiredAccuracy =kCLLocationAccuracyBest;
            self.locationManager.distanceFilter =kDistanceFilter;
            self.locationManager.headingFilter =kHeadingFilter;
            self.locationManager.pausesLocationUpdatesAutomatically =YES;
            self.locationManager.activityType =CLActivityTypeFitness;
        }

desiredAccuracy: 想要获得的定位精度, 会尽可能地满足设定的精度, 但不能保证在实际过程中能达到.
distanceFilter: 低于水平距离会过滤掉而不产生更新事件.

开始定位服务:

[self.locationManagerstartUpdatingLocation];
[self.locationManagerstartUpdatingHeading];

当获取到位置信息或位置产生变化时会通知代理

获取到新的位置:

locationManager:didUpdateLocations
方向产生变化时:

locationManager:didUpdateHeading: