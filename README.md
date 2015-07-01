#What we have learned so far at DevLeague

##Arrays and their methods
Array are groups of data housed within brackets and separated by commas. They can store all kinds of data, functions, objects, other array, numbers strings, booleans etc. Just like strings, each index of the array can be accessed using the zero based index system. Additionally, there are many methods that are automaticlaly built into JS that can be used on Arrays. Be careful! Some of these methods will mutate the original array, while others will just access the values in them.


##Chrome Debugger
On a mac, you can open up your Chrom Dev Tools using the cmd + option + j shortcut. (Or you can right click and select inspect element) There is a ton of stuff you can do in your dev tolls but if you navigate to the 'sources' tab, you will be able to see the source files and view the acutal code for the page you are on. You can create break points in the code that allows you to stop the functionalaity of the code, and 'step-into' the code. It is really useful if you are trying to debug a particular function that you wrote. You can run the JS interpreter line by line or go step by step if you need too. You can also add the word debugger to your actual code and the Dev tools will automatically stop at that point while executing your code. **Make sure to remove all debuggers from your code prior to production**


##Scope
Not just a name of a mouthwash but also a concept in JS that restricts variables from being used on the global scope and other scope. It limits variables to only be accessed when you are in the same 'scope' or room as them. Any new variables created inside a function can only be used by that function. From a visual perspective, if you have a function within a function within a function (3 functions) the all of them have new varaibles declared in them, the deepest functions will have access to all of the variables, while the first function will only have access to the variable declared prior to the second function. If the functions are laid out horizontally, scope goes right to left. If you start on the right (fuction 3) and move to the left, all varaibles can be access. If you start on the left and move to the right, you can only access the variables prior to the second function.


##Hoisting
Hoisting is when the JS interpreter moves around your code to the order it should be run. Will move all globally assigned functions and variables to the top, prior to executing your code.


##Objects
In JS everything is an object. Objects are groups of data that have similar properties. In the real world a hockey stick is an object. It has brand, model, flex, weight, grip and curve properties. In JS you the objects properties are called its keys and store its values. It looks like this:
```
var hockeyStick = {
  brand : 'Reebok',
  model : 'Ai9',
  flex : 100,
  weight : 1000,
  grip : true,
  curve : 'Nash'
}
```
Values of an object can be strings, numbers, booleans, objects, function (AKA methods), truthy and falsey. In order to access the values of an object you should use dot notation or brackets with the key name in quotes.

 Here is a helpful video to get your going [Helpful Video](https://www.destroyallsoftware.com/talks/wat).

##Strict Mode
You can implement 'strict mode' in your files by invoking a strict mode function at the top of your document. Inside the strict mode function you place the words strict mode in quotes. All of yoru code hsould follow that line within the function. If you stay inside the function your code will be in strict mode. Strict mode will throw silent errors, prevent you from using certain syntax and generally makes it easier to write secure code.


##Using this


##Module Patterns
Modules patterns can be used if you want to create privacy for variables, functions, or objects and its properties. In order to use mod-pats you create a function and inside that function you return an object. Any methods or variables inside that function are not directly visible/accessible by calling that function. The object that is returned will reference the private variables or methods you declared. On the other hand if you want to leave them private, you don't need to refernce them in the object that is returned.


##Closures
Closures are used to 'close off' certain variables/functions to the global scope. Limiting access of the variables to the local scope. They are used in module patterns to 'hide' or restrict access to the private variables.


##Linked Lists Data Structures
See great blog post about this here:[Linked Lists: The trains of JS](https://medium.com/@Rastalamm/linked-lists-d54a770dcdd2)


##OOP in ES6



##Prototypes and Inheritance


##OOP in ES5


##Call, Apply & Bind
The call bind and apply methods enable you to use a prototype function of another object with your current object. So if your Person object has a prototype method of walk, you can call/apply/bind the walk method on a new object. You can also use them to force context inside of another function.
####What's the difference between Call, Bind & Apply?
Call and Apply are nearly the same. They both invoke the function immediately but Call takes a list of arguments while Apply takes an array of arguments.
Bind calls a function at a later time based on when a certain event occured. Bind works like call in that it takes a list of arguments.


##Testing
You always want to write tests for your code so as you add code and grow, you can see if any of your new code conflicts with any of the features or functionaly of your old code. If you write your tests first, it forces you to think about how your will use your code prior to writing it. It helps you to understand the overall project and task you are trying to complete.

###TDD & BDD
TDD stands for Test Driven Development. Think should. Your code should do this.
BDD stands for Behavior Driven Development. Think expect. Your results are expected to look like this.

Both cycles contain 5 steps.
* Start with a list of your requirements
* Write a test for one of your requirements. Be specific. The more the merrier
* Make sure your tests fail.. wait for it.
* Write your code to make it pass!
* Refactor (if necessary)


####Mocha
Is one of the many JS testing frameworks. It runs Node on your computer and in your browser. Two main functions when writing your tests. decribe() and it(). describe() groups your test cases into test suites. it() is where you write your individual test cases. Hooks allow you to set up your state before and after functions. You can set it to run before/after each test or before/after only 1 test block.

####Chai
Chai is an assertion library for node and the brswer that can be paried with ANY JS testing framework. Chai makes the tests read like English. There are words designated as 'chain' words that chain your assertions together so they can be read easily.


##Arrays Iteration Methods / Functional Programming
The below list of Arrays are called Iterator arrarys. They do just that; loop over the arrays. They make up part of the Functional Programming foundation.

With functional programming, you just return results, instead of storing data in variables and continuously accessing the stored data.

* forEach(function(c, i, a)) - calls a funciton you provide for each element in the Array
* every(function(c, i, a)) - returns true if EVERY element in the Array passes the test you provide.
* some(function(c, i, a)) - returns true if ANY element in the Array passes the test you provide.
* map(function(c, i, a)) - creates and returns a new array with all the element that pass the TRUE test
* filter(function(c, i, a)) - creates and returns a new array with all thereturned values from the callback function
* reduce(function(p, c, i, a)) - returns a single value accumulated against all values from the callback function.
* reduceRight(function(p, c, i, a)) - its the same as the previously mentioned reduce function but starts from the right side of the input array.

##Static Methods
Static Methods are functions that are built on the class and cannot be extended.

##Inheritance and Interfaces
Mixins are design patterns that are used to allow multiple inheritance in JS. Essentially you create a class of multiple objects' properties. There is no limit as to the number of other objects' properties we can grab/share from. We don't inherit any consturcotrs in the mixin. Use a mixin if you want to inherit a behavior from multiple objects.

####Interfaces
Interfaces allow us to define a contract/blueprint. If any object implements an interface, it must provide certain behavior and properties. All in all its just a contract. "if you want to be in the band, you gotta wear the makeup"


##The DOM


##Recursion



##Curry


##Callbacks


##Typescript


##Bubble Sort
The least efficient way to sort items in an array. Bubble sorting compares two items in an array, and switches their places based on their value. It does this on each iteration and will slowly move the highest values to the right and the smaller values to the left. It take a lot of time and energy to use this method. You can use a loop to compare the first value to the second value and switch there places based on ther value.

##Quick Sort
Quicksorting is another sorting method that sorts an array by selecting a value to compare against, also known as a pivot value, and partitioning the remaining values to to left and right of the partition value. Using recusion, this is completed until there are no more values to split. On the recusive way up, it concat's the arrays into the sorted value. The keys words are:
*Pivot - the value you are comparing against to determine the two partitions.
*Partition- each time a split occurs they end up in two paritions (sections/sides) - left and right.
*Recursion - For each partition we recursively pass it inside the splitting function, thus generating new pivot, left and right values.
*Concatenation - Concatenate the left, pivot and right array which outputs a sorted array.
On every iteration of our quicksort recursion we know that our pivot is greater than all values to the left and less than or equal to the first value on the right.

##Factory Pattern
Another design pattern



##CSS


##SASS / Scss



##Ajax


##Node
###Debuggin JS
###Events / Emitters



##Streams



##Markdown Editor Resources:
https://help.github.com/articles/markdown-basics/
http://daringfireball.net/projects/markdown/syntax
http://dillinger.io/