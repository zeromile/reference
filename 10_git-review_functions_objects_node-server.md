# 10 - Git review, Functions, Objects, Node server #


Git review

Create a repo and clone

Commit



FUNCTIONS

Show how to send multiple variables to a function

show what happens when you set up for one variable but send two, and vice versa

Show what a return does

Show how to create a function that creates a reference to 

Challenge: Create 5 buttons and then code that will change the background color of the clicked button to green and all the others to red


OBJECTS


http://www.w3schools.com/js/js_object_definition.asp

Objects contain properties (size, weight, color, etc) and methods (functions/actions)

'''var object = {
	brand: ‘volvo’,
	start: function() {
		console.log(‘Started car’);
		}
	}'''




First node server

Install Node from the Web site

Verify its installed with node -v

launch the REPL (read-eval-print loop)

Clone WestHillsGeekwise/jrp10

—— app1.js ——
var http = require('http');
http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
}).listen(1337, '127.0.0.1');
console.log('Server running at http://127.0.0.1:1337/');
————————

in terminal, navigate to the jrp10 folder and type node app1.js

Open a browser and navigate to the URL specified in the REPL

Challenge:
1. change the output text
2. Try some html
3. Change the console message

Talk about require(‘http’)

talk about createServer()

Talk about writeHead()



—— app2.js ——
this will read and return a file

describe the flow of data

Talk about readFile()




