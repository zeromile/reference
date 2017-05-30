# REF: DIF MODULE VS PACKAGE #

From: http://stackoverflow.com/questions/20008442/difference-between-a-module-and-a-package-in-node


Module's are libraries for node.js. See the below excerpt from the node.js api:	Node has a simple module loading system. In Node, files and modules are in one-to-one correspondence.	Examples of modules:		•	Circle.js
* Rectangle.js		•	Square.js	A package is one or more modules (libraries) grouped (or packaged) together. These are commonly used by other packages or a project of your own. Node.js uses a package manager, where you can find and install thousands of packages.
Example of a package:	Shapes             <- Package name
  - Circle.js      <- 
  - Rectangle.js   <- Modules that belong to the Shapes package
  - Square.js      <-	Essentially, you could install the package, Shapes, and have access to the Circle, Rectangle, and Square modules.
shareimprove this answer	answered Nov 15 '13 at 19:23	
￼
	making3
3,40441930
	add a comment


￼
up vote	3	down vote	Every Node app is a package, and should have a package.json file. Those apps that act as middleware (or the equivalent of libraries), and are meant to be installed inside other apps are modules.
In short all modules are packages, but not all packages are meant to be used as modules, though many can be.
Modules will be installed, if listed as dependencies in the package.json file, and placed into the node_modules folder, but npm recurses through their package.json files to add the modules they rely on.
shareimprove this answer	answered Nov 15 '13 at 19:18	
￼
	Jason Nichols
1,9451235
	add a comment
up vote	0	down vote	Everything what you can require() is a module. In most cases in the CommonJS world it's one file is a module.
A package can contain several modules, but you usually loading the entry point (main), which is specified in the package.json or it's index.js if no main property is provided, for instance: require('express')
But you can also require another file (not the main file) if you know the location, for instance: require("express/lib/application") (in node.js you can omit the extension: .js)
A package can access modules from other packages if they are listed in the dependenciesproperty of the package.json.
Actually npm installs all the packages into node_modules which is confusing, because it should benode_packages.
https://nodejs.org/api/modules.html
