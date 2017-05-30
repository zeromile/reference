# REF: Angular notes Workshop #

Forms can be Template Driven or Model Driven

Angular JS Terms
Modules - Represent components in your applications, makes it easier to reuse code
Directives - allow you to extend html tags which will make it easier to bind your html to data
Scope - Javascript objects used to represent data - which can come from a database or other web/local source (when you see “scope” think “data”)
Expressions - directly linked to the scope, data binding  e.g. {{expression}}
Services - things that perform tasks

AngularJS works with the DOM

Template - Model - Controller

```
var app1 = angular.module(‘app1’, []);
```

Defines an AngularJS model. Modules are use to associate an Angular JS app with a part of an html document. They also provide access to Angular JS features and help with organization.

The Angular module is going to accept a module name (‘app1’) as well as a list of modules ([]) in order for the app to function properly. A third parameter can be included after the modules list for optional module configuration.

```
<html ng-app=“app1”>
```
or
```
<body ng-app=“app1”>
```

Instantiates the Angular code. It tells the AngularJS application that all the stuff inside this element (between the opening and closing tag) is part of the ‘app1’ application (app1 is the module name).

```
<html ng-app=“app1” ng-init=“person = {fName: ‘Jason’, lName: ‘Cooksey’}; capitals[{city: ‘Sacramento’, state: ‘CA’}, {city: ‘Sacramento’, state: ‘California’},{city: ‘Montgomery’, state: ‘Alabama’},{city: ‘Phoenix’, state: ‘Arizona’}]”>
```

ng-init Is a directive that initializes the application data by assigning values to variables.

```
<div ng-controller=“ctrl1”></div>   <— This is going to be a “view” (as well as all the elements inside of it) and we will use scope component to provide data to the view
```

To define the controller:
```
app1.controller(‘ctrl1’, function($scope) {
	$scope.first = 1;
	$scope.second = 1;
	
	$scope.updateValue = function() {
		$scope.calculation = $scope.first + ‘ + ‘ + $scope.second + “ = “ + (+$scope.first + +$scope.second);
	};
})
```

‘ctrl1’ Is the name of the controller and function() is a “factory function”. Factory function gets the controller ready to use and  $scope is a dependency and it’s placement in the attributes here is telling Angular to automatically pass in the $scope object whenever the function is called. Angular is smart enough to know what we want and it’s going to throw it in there automatically for us. This is “dependency injection”. 


We can use a $scope variable name in an expression (it will be empty if it’s in a $scope function that hasn’t been called yet) or we can use a $scope function in the expression which will call it automatically.

```
<button ng-click=“myCalculation”>Calculate</button>
{{calculation}}
```
vs
```
{{myCalculation()}}
```
(in the first instance myCalculation() sets the variable calculation, in the second instance myCalculation() returns the value of the calculation)
