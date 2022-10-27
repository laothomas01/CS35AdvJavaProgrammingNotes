
# List of topics learned:
- build reference model object
- load reference model using fileIO
- archive reference model using Serialization
- code containment using inner classes
	- ![[Pasted image 20221026193631.png]]
	- what can be observed here? 
		- option class is a box containing a smaller box, *option class*, and instances of option class.  
- noticing patterns in a software structure information
	- *from a higher class hierarchy perspective*
		- option set class has a 1 to many relationship with option class instances
		- automobile had a 1 to many relationship with an option set instance
		- option class is an atomic component for higher level classes
- recognizing relationships between classes:
	- (note: think of the code contaiment similar to russia dolls)
	- class hierarchy and encapsulation
		- the higher the level, the more available access is to the lower level class' functions
			- access to lower level can only happen through the higher leveled class
		- the lower the level, the more inaccesible a class becomes
		- code containment
			- inner classes
				- a class within another class
				- closely related classes belonging to each other
				- keeps the most atomic class hidden away from public
		
- using the *protected* access modifier
	- why? 
		- hides away backend code. 
		- forces users to use functions you make accesible
		- e.g 
			- think about how the human body works.
			- our brain is already a higher level class that gives functionality to everything in your body such as motor skills.
			- motor skills, memories, blood flow, water levels, etc...  are all hidden away as backend components and data unable to be touched or understood or read unless someone gains access to your brain and manipulates the class. 
	- how? 
		- set a class's access modifier to public
	- when?
		- when information is highly sensitive and you want to determine who has access to what kinds of information or functions
	- what?
		- protected access modifier means you can only access those classes and functions if they are in the same package as invoking class.
			- e.g 
				- model package contains automobile, optionset and option class
				- fileIO contains readData class and cannot access optionset and option because they are protected. 
				- fileIO can access them through automobile because automobile is public and contains a collection of instances of those protected classes. 
	- where?
		- 
- Using class diagrams to depict relationships between classes, and input/output of data 
- class packages
	- Model
	- Util
	- Documents
	- FileIO
- writing flexible code
	- functions can use each other if there is a generalized enough functions with branching possibilties of usage
		- e.g
			- getting an instance of a class leads to many reusable opportunities
			- ![[Pasted image 20221026203130.png]]
	- chaining constructors
		- ![[Pasted image 20221026203034.png]]
# After thoughts
- can i associate this lab with video games?
- why serialize?
# Supplemental Review Questions
Car Configuration Application Reflection Questions on Assignment
- You should review following questions to make sure you understand the outcomes from Unit 1.
	- You should document lessons learnt for submission (with final unit of Car Configuration Application). 
	- You do not submit these questions for grading: 
		1. What is the relationship between containment and encapsulation (as applied in this project), when building components? 
			1. containment - a class/box acting as a box for another class/ box
			2. encapsulation - you can only access an inner box through the instance of a class containing that box
		2. What are some ways to analyze data (presented in requirements) to design Objects? 
		3. What strategies can be used to design core classes, for future requirements, so that they are reusable, extensible and easily modifiable? 
		4. What are good conventions for making a Java class readable? 
		5. What are the advantages and disadvantages of reading data from sources such as text files or databases in a single pass and not use intermediary buffering? 
		6. What is the advantage of using Serialization? What issues can occur, when using Serialization with Inner classes? 
		7. Where can following object relationships be used: encapsulation, association, containment, inheritance and polymorphism? 
		8. How can you design objects, which are self-contained and independent?




### Summary of topics learned
- **code containment**
- encapsulation
- **using protected access modifier**
- why use inner classes
- **writing flexible code**
- using class diagrams to flesh out logic of system design
- serialization/deserialization
- file IO.
- how to handle the protected access modifier
- how deep of a rabbbit hole can you travel for code flexibility?
- **generalizing the relationships between classes, functions, or even data.**
- **compressing code down through generalizations/pattern recognition**
- try out new tools and approaches instead of feeling frustrated.

HOMEWORK: finish summary of lab 1




