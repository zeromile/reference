# 15 - Angular, common directives, working within express/node #


Angular is an MV* framework. Enforces separation of concerns. It allows you to enhance behavior of your HTML tags. 

### Modules ###
represent components in your application - makes code reuse easier

### Directives ###
Allow you to extend html tags and attributes…makes binding data to the html very easy

### Scope ###
Angular will use objects to represent data, called the scope, which can be data generated on the web server, or database or web service

### Expressions ###
Are directly linked to the scope (data) and will be updated dynamically as the data changes (data binding)

### Services ###
The things that do stuff



ng-app=“” sets the app name in the <html> or <body> tag

adding ng-init initializes the application data…e.g. ng-init=“person = {fName: ‘Derek’}”


Show how to use scope to pass variables from the index.js file to html page…then use built-in angular directives to do stuff

ng-if, ng-show, ng-hide, ng-class (use JSON object to set conditional formatting)
 

ng-cloak will hide an element until angular has finished rendering

