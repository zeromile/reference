# 09 - Loops (cont) #

Loops iterate through something. We can use a loop to repeat statements, or to look and act upon at each element in an array.

for
A For loop allows us to repeat a statement or block of code for a specified count

	for(var i = 0; i < 10; i++){
		console.log(i);
	}

….or….

	var numbers = [33,21,2,45,5,6,2];
	
	for(var i = 0; i < numbers.length; i++){
		console.log(numbers[);
	}


while
A While loop allows us to repeat a statement or block of code for a specified count
	
	var i = 0;

	while(i < 10){
		console.log(i);
		i++;
	}


forEach
The forEach function is a method of arrays. It is specifically for arrays to allow you to walk through them index by index

	var numbers = [33,21,2,45,5,6,2];
	numbers.foreach(function(number){
		console.log(number);
	});

….or….

	var numbers = [4, 9, 16, 25];

	function myFunction(item, index) {
    		console.log(demoP.innerHTML + "index[" + index + "]: " + item + "<br />”); 
	}
	
	numbers.forEach(myFunction);


Challenges

1. Single button text replace
    1. Make a button with the text “Submit” that, when pressed, changes it’s own text to “Thanks for submitting”
2. Multiple button text replace with single function
    1. Make 5 buttons “Click me”
    2. Make an array with 5 names
    3. Button click should replace the text of the button with a randomly chosen index from the people array
    4. The button text should be changed using a single function that uses conditional FOR to find which button was pressed and change the text accordingly
3. Array Add
    1. use forEach to add all values in an array
4. Calculator2
    1. Make a form that allows you to enter 5 numbers in input fields
    2. Create an “Add” button
    3. When you click on the add button 
        1. the 5 input values should be written to an array 
        2. the 5 values in the array should be added together using the forEach
        3. BONUS: use a for loop to grab and write to the array all 5 input values

Objects

Creating an object

person = {
first name:”Jason
}

vs

person = new object();  //valid but not really used



