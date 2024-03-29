## Summary
- custom exception handler
- learn about how and why use interfaces
- learn about how and why use abstract classes
- what is difference between abstract classes and interfaces
- what is the "self healing software" feature we created?

# Lab Part 1
- ## using abstract class, interfaces
	- use abstract class to encapsulated instances of our automobile class
	- let's create a class that extends the abstract class called BuildAuto so it can instantiate those encapsulated instances
	- let's create interfaces: why?
		- interfaces are a way for developers to determine which class methods from the backend should be public
		- we make a 'create auto interface', a 'fix auto interface' and an 'update auto interface'
		- create auto - contains a build auto function used to instantiate the automobiel class and a print auto to find an automobile and print its values
		- fix auto - for handling software exceptions
		- update auto - update the values of the automobile such as name and price
		- e.g
			- ![[Pasted image 20221027171608.png]]
	- the abstract methods within these interfaces are implemented into the build auto class
		- we define the function of those abstract methods based on the methods we defined within classes such as automobile, and fileio.
		- e.g 
			- ![[Pasted image 20221027171422.png]]
			- ![[Pasted image 20221027171531.png]]
			
- the overall picture to paint here:
	- in lab 1 we created a backend with FileIO to load data, and base model reference to perform CRUD operations. 
		- we also made the option and option set class protected and had to re-define the functionalities of those class' functions inside the automobile class therefore creating a high level of abstraction: we know there is some functionality happening in the back end by looking at the automobile class but we dont really know what is behind the scenes.
	- in lab 2 we are building an API(application programming interface)
		- in our interfaces, we specify the methods from public classes we want users to use while hiding away knowledge about our backend
		- our build auto class is contracted by the interfaces it implements to find uses for their abstract methods
	- we divide functionaltiy between interface and abstract class:
		- the interface is for making methods we want public
		- abstract class is for acting as an encapsulator for instances of classes related or associated to the automobile class
	- 
# Lab Part 2
- self healing software:
	- fix auto interface:
		- ![[Pasted image 20221027171655.png]]
- ## Part 1
	- ### Abstract Method
		- method that has no body
		- sub-class must implement the method
		- always public
	- ### Abstract Classes
		- what functions do you want sub classes to expose?
		- class can only extend 1 abstract class
		- if many closely related entities have common functionalities, use an abstract class
			- i.e Enemy and Player extend abstract class Entity.
			- Entity contains common functions such as attack, heal, defend.
			- both Enemy and Player can defend, attack and heal
		- can define abstract methods
			- contractually has to be implemented 
		- can be used to encapsulate instances of closely related classes
			- i.e abstract classes
	- ### Interfaces
		- used to expose methods from sub classes
			- these become APIs
		- classes can implment multiple interfaces
		- contains methods you decide are to be public
		- variables are final type
		- adds functionality to unrelated classes
			- i.e Player can swim so it implements swimmable interface
		- doesnt have to define abstract methods
			- can be used as just a type extension
		- can define abstract methods
		- can be used to define classes are specific types of entities
			- Player is SWIMMABLE but Enemy is not
	
	- ### Abstract Classes vs Interfaces
		- both can define abstract methods
		- abstract classes allow for creation of regular methods and variables alongside abstract methods
		- abstract classes can keep adding non-abstract methods without forcing a contract by sub-class to implement it
		- interfaces force a contract by sub-class to implement its methods
- ## Part 2
	- ### Custom-Exception Handling Class
	- custom exception ![[Pasted image 20221027173305.png]]
		fix interface 
	- ![[Pasted image 20221027173326.png]]
		 implementing fix interface ![[Pasted image 20221027173400.png]]
	-  fix function ![[Pasted image 20221027173448.png]]
	- encounter error, throw and catch exception. 
	- log error number into .txt file
	- locate error number in fix function and fix the problem
	- ![[Pasted image 20221027173021.png]]
	- run software, encounter error and re-run software until problem is fixed
		- ![[Pasted image 20221027174317.png]]
	1) let's handle improper loaded data such as malformed automobile price
	2) throw the exception if such an error occurs
	3) catch the exception
	4) log exception number by caching to .txt file
	5) read error numbers in .txt file 
	6) based on those numbers (or some way to handle the recorded error numbers) create methods that represent the functions to fix the sotware
	7) when running build auto, run function, encounter exception, fix, and re-run(recursion?) until all errors are fixed
	- ### "Self-Healing Software"
	- its an algorithm that search for the potential solution based however you write your solution
	- there should be a limit to how long you must attempt to find your solution and break if there is no solution
	- algorithm points out where the solution is at what location