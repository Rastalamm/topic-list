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
Whenever a function is invoked, there are always two implicit parameters passed into the function; this and arguments. arguments is an array of the arguments. EX: arguments[0] = the first argument passed in. this refers to the object which the current function is associated or belongs to. AKA the function context. this always always always refers to an instance of an object and a function always belongs to an object. If the function is on the global scope, this will refer to the global object whereas if the function is a method of an object, this refers to the object.


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
Chai is an assertion library for node and the browser that can be paired with ANY JS testing framework. Chai makes the tests read like English. There are words designated as 'chain' words that chain your assertions together so they can be read easily.


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
DOM stands for The Document Object Model. It is the interface where we can manipulate the the structre and style of a document. The DOM is an API for interacting with the browser. It is a dynamic, in-memory representation of an HTML document.

###How it works..
1. The browser requests HTML document from the server
2. The file is dowloaded to the browser as plain text
3. The browser parses the HTML text to create the DOM

It is good to note that you cannot change the source file, rather all the changes/mutations are made to the DOM itself. Being a JS dev, most of the changes we want to make are done on the document or window properties (and their children) of the DOM. Anything that is written in HTML/CSS can be done via the DOM and JS. The DOM structure is laid out in a way that all the elements are ancestral in nature and have relation. Meaning, elements can have parents, children siblings and so forth..

###document
The document represents the HTML elements and Styles/Attributes that are applied to the elements. We can change all aspects of the doucment as needed.

###window
The window repressents the current browser window as a whole, including current URL, history, screen dimensions etc..


##Recursion
Recursion is the action of a function calling itself inside its scope. Yes. I know.

Why would you use it? - Simple. We use recursion when we have an input structure to our function that can be of infinite dimensions. When out input to our function is going to be similar in type, but differing values repeatedly.

In order to use recusion properly, there are a few key aspects to remember.

Base Case: The most important one and allows you to break out of recursion. It is the point at which the input value stops the funciton from calling itself, in order to "unwind" it's returns.

1. Always define base case so you don't run into an infinite loop
2. Make sure the input is changing each time you recall your function
3. Once a function returns, hits the base case, the call stack will unwind and finally exit from it's initial call. Every function call will return during the unwinding.

##Curry
Currying is the process of converting a function that accepts multiple arguments, into one that accepts a single argument, by binding some of the arguments into the original function. Why? We want to stay DRY when invoking funcitons that use the same arguments many times. The goal is for each function to take at most one argument. Below are a few ways to implement currying.

1. Manually - Write a function that returns another funciton that accesses the argument of the original function. The original function arguments change the result of the returned function when its invoked.
2. Using a curry helper - Use a helper function to convert functions into a curried function that accepts a single argument.
3. Using Lo-Dash Curry Helper - lo-dash's partial() function to convert functions into a curried function that accepts a single argument.

##Callbacks
A callback is any function that is passed as a parameter to another function. Function 1 has a parameter that is function 2. A callback is a function that is called when something (usually and event) happens. When the event happens, the callback function is called.

An analogy: You go to the store and ask the person for a box. Instead of waiting around for the box, you go around the store. Once the box is ready, you can get it from the person.

Common types of callbacks are setTimeout and setInterval. Callback functions are asynchronous functions and don't follow along the traditional synchronous top to bottom approach.


##Typescript
A free, open-sourced programming language developed and maintained by Microsoft. It is a typed superset of JS that complies to plain Javascript everywhere. The two main goals of Typescript are:
1. to statically identify constructs that are likely to be errors
2. To provide a structuring mechanism for larger pieces of code.


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
CSS stands for Cascading Style Sheets. It is used to define the look, format and layout of HTML elements. CSS is based around Specificity. When giving properties to elements, you need to define which elements are to receive which styles. In certain cases, some elements will have conflicting styles attempting to be apply their property on the element. Specificity defines which style will be applied to the element. The below list is the order of specificity from the most specific (highest) to the least specific (lowest)
1. Style on HTML element Ex: ``<``div style='...'
2. ID Ex: #elementID
3. Class Ex: .elementClass
4. Tag Ex: div, h1, p

Specificity states that the most specific matching rule will be applied. In order to over ride specificty, you can use the !important tag. It will apply that style to the element. Another unique selector is :pseudo. Pseudo selectors are styles that are applied to elements with a certain state or relation. Ex: hover, clicked, first-child. Lastly, there are certain Vendor Prefixes. Vendor Prefixes came about as certain browsers started implementing support before others so that developers could target their browsers while offering fallbacks for other browsers. Always test your CSS on the browsers you want to support.

When planning a layout you should implement the below:
1. Good wireframes
2. Good markup
3. Think about mobile/ responsive
4. Style for structure (setting borders/backgrounds)
5. Style for spacing
6. Style Type
7. Style Images

##SASS
A css compiler. It is just like CSS but adds additional features that are beneficial for when your application/files grow in size. Features such as variables, nesting, mixins, partials and inheritance will make it easier for you to make quick changes and build with ease.

####Preprocessing
Your css is written in a .scss file. The markup will be processed out to a regular.css file.

####Variables
Just like a JS variable, in SASS you can define a variable. An css value can be defined as a varialbe. It is especially useful for values that are the same, but used in many locations (think colors, padding etc..).

####Nesting
Nesting gives you the ability to write your css in a nested structure; similar to HTML. Helpful to read, but be careful to keep track and maintain your indentation/nesting.

####Partials
SASS allows you to create partial files that house smaller bits/snippets of css. I place my clearfix and reset files in snippets. You use the @import command at the top of your SASS files to include them.

####Import
This is the same as using the @import option in CSS but instead of requiring an http request (like in css), SASS will combine it with the file so it's served as a single CSS file in the web browser.

####Mixins
A mixin allows you to make groups of CSS declarations that you want to reuse throughout your site. Mixins are helpful for vendor prefixes. You can also pass in varaibles to make them dynamic/flexible.

####Extend/Inheritance
Using an @extend command lets you share a set of CSS properties from one selector to another. Helps keep your code DRY.

####Operators
Using operators in your scss files allows you to do math in your CSS. Makes converting to percentages easy.


##Ajax
Ajax stands for Asynchronous JavaScript and XML. AJAX allows us to transfer information (data) from the web server to the application, and visa versa, without having to refresh the page. We are no longer making XMLHttpRequests; Today they are called HTTP requests. JSON(JavaScript Object Notation) is the primary standard for transferring data via REST API's.

The two primary ways that use AJAX are Native broswer XmlHttpRequest API and JQuery $.ajax()method . The easier and method with more cross compatibity is the jQuery method. In order to make the request you need to include the following three items:
1. method - the HTTP request method (GET, POST, PUT, DELETE)
2. url - the URL to send the request to
3. dataType- 'json'

Upon sending the request, you need to listen for a response. There are 3 methods to this.
1. .done() - handle the successful response
2. .fail() - handle the failure
3. always() - Always update the UI

With jQuery, you need to make sure you are using the correct implementation/documentation for your version. Below are some additional jQuery methods for you to make a specific request.
* $.getJSON()
* $.get()
* $.post()
* $.getScript()
* $.load()


##Node

###Debuggin JS
###Events / Emitters



##Streams



##Socket Server



##HTTP Server


##Query String



##SQL / Databases

###PostgreSQL

[PostgreSQL Data Types](https://medium.com/@Rastalamm/postgres-data-types-f6366cd2e562)

## Web Application Framework: Express
A web application framework is a basic structure that supports the commonalities of the necessary components that make up a web app. They hide the boilerplate and infrastructural code related to handling HTTP requests and responses.

###What is Express?
Express is a light weight web app framwork that helps organize an MVC architecture on the server side. (MVC stands for Model View Controller). We use Express so we do not have to repeat the same code over and over again.

###Model View Controller
A way to logically separate the different responsibilites of the application. It also defines the interactions between the three sections. The benefit of using this pattern is that you are separting your app into different sections so they can be managed easier. If everything is in one file/location, it is hard to identify where ceratin actions are happening. Be splitting it up, your code is laid out in an organized fashion.

* Model: How do we represent the data? For example, how do I go from my objects to a persistent storage such as a DB -> how do I save my 'User' object to the database? (Think Database Tables)
* View: How do I render the result? They get all the information and dynamically generate the HTML representation of the page.
* Controller: What am I doing? This is the action that's taking place, and what, on a conceptual level, needs to be carried out. For example, what stages do I need to go through to invoice a User? Contains the business logic of the app and operate on the models.


###Middleware
Middleware is a function with access to the request object, the response object and the next middleware in the app's request-response cycle. Middleware can:
* Execute any code
* Make changes to the request and the response objects
* End the request-response cycle
* Call the next middleware in the stack

If the current middleware does not end the request-response cycel, it must call next() to pass control to the next middleware function. If you do not call next() the reqeust will hang.

There are different kinds of middleware
* Application-level
* Router-level
* Error-handling
* Built-in
* Third-party

YOu can load application-level and router-level middleware with an optional mount path. You can also load a series of middleware functions together.



##ORM's : Sequelize


##Template Engine: Jade


## RESTful API's

##Authentication

Authentication - Identify a person
Authorization - Access to resources
Basic Auth

local-strategy
Store user information: username, password
use a one-way hashing algorithm

use crypto hashes
blowfish
1. its slow, you cannot easily guess, bruteforcing would take infeasble amount of time
2. one way, is not decryptable
3. if two hashes are identical, confidence that they are the same message
4. has collections are mathematically improbable.

Sessions
authenticate w/ username and passowrd
server stores a key and send you a key in the form of a cookie
once you log out the session is ended


OpenID is a federated Auth System - have someone else deal with authentication only
OAuth - delegated auth system - has someone else deal with authorization

##Meteor

##AngularJS


##Markdown Editor Resources:
https://help.github.com/articles/markdown-basics/
http://daringfireball.net/projects/markdown/syntax
http://dillinger.io/
