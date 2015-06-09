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




##Strict Mode



##Using this


##Module Patterns



##Closures
Closures are used to 'close off' certain variables/functions to the global scope. Limiting access of the variables to the local scope.


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




Markdown editor Resources:
https://help.github.com/articles/markdown-basics/
http://daringfireball.net/projects/markdown/syntax
http://dillinger.io/
