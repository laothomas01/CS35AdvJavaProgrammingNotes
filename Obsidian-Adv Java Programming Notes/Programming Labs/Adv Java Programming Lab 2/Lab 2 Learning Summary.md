## Summary
- custom exception handler
- learn about how and why use interfaces
- learn about how and why use abstract classes
- what is difference between abstract classes and interfaces
- what is the "self healing software" feature we created?

# Lab Part 1
- ## using abstract class, interfaces
	- in lab 1 we 
# Lab Part 2

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
	- ### Custom-Exception Handling
	- 
	- ### "Self-Healing Software"
	- its an algorithm that search for the potential solution based however you write your solution
	- there should be a limit to how long you must attempt to find your solution and break if there is no solution
	- algorithm points out where the solution is at what location