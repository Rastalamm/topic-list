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


##Testing
TDD & BDD
Using Mocha & Chai




##Advanced Arrays / Functional Programming


##Static Methods and Inheritance
Mixins

##The DOM


##Recursion



##Curry



Markdown editor Resources:
https://help.github.com/articles/markdown-basics/
http://daringfireball.net/projects/markdown/syntax
http://dillinger.io/
