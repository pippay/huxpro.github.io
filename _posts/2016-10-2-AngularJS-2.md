---
layout: post
title: AngularJS-2
categories: [js框架]
tags: [AngularJS]
description: Angular JavaScript
---

### AngularJS 服务(Service)

有个 $location 服务，它可以返回当前页面的 URL 地址。

```
var app = angular.module('myApp', []);
app.controller('customersCtrl', function($scope, $location) {
    $scope.myUrl = $location.absUrl();
});
```
