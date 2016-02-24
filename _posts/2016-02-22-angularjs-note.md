---
layout: post
title: Angularjs reload page
category: Angularjs
comments: true
---


*Common solutions to problems for angualrjs*

## Reload page

```
<button data-ng-click="reloadRoute()">refresh page</button>
```
Usually, you can use the reload method of the ```$route``` service. Inject ```$route``` in your controller and then create a method ```reloadRoute``` on your $scope.


```
$scope.reloadRoute = function() {
    $route.reload();
};

```

If you are using **angular-ui/ui-router** you can use the following method to reload the current state / route. Just inject ```$state``` instead of ```$route``` and then you have:


```
$scope.reloadRoute = function() {
    $state.reload();
};

```

Note: Above methods just refresh js files, the following method will cause the current route to reload. If you however want to perform a full refresh, you could inject ```$window``` and use that:


```
$scope.reloadRoute = function() {
   $window.location.reload();
}

```
