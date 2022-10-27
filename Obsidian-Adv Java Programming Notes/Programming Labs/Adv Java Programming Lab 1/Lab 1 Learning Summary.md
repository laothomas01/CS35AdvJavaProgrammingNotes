
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
			1. you can look at which object encapsulates or uses another class or an instance of that class
			2. for the car configuration data, you have to think about the the relation between an optionset class instance and its containment of multiple option class instances
				1. option set class has a 1 to many relationship with option class
				2. this also applies to the automobile class
					1. the automobile class is a 1 to many option set class relationship 
						1. each option set class instance contains many option class instances
		3. What strategies can be used to design core classes, for future requirements, so that they are reusable, extensible and easily modifiable?
			1. think about what use the class has beyond being a container for data
				1. 
		4. What are good conventions for making a Java class readable?
			1. the name should specify the functionality of the class or variable
			2. class names always start with capital letters
			3. variables/instances are camel cased
			4. methods are camel cased
		5. What are the advantages and disadvantages of reading data from sources such as text files or databases in a single pass and not use intermediary buffering? 
			1. referential link: https://medium.com/@isaacjumba/why-use-bufferedreader-and-bufferedwriter-classses-in-java-39074ee1a966#:~:text=It%20is%20recommended%20to%20use%20BufferedReader%20if%20you%20want%20to,threads%20when%20using%20Buffered%20Streams.
			2. disadvantage: 
				1. it takes up a lot of memory and is highly costly in performance to read/write without a buffer
			3. advantage: better performance. store your input data into a buffer and flush that buffer by outputting it somewhere.  
		7. What is the advantage of using Serialization? 
			1. turns an existing object into a byte array which can by used between JVM's running the same code to transmit/read the object
			2. communication between two machines: 1 machine converts the object into byte array and the other machine decodes it to use that data. 
			3. when running application, all objects are stored in RAM. when you exit, your memory forgets everything that happened during run time. serialization lets you save application save objects to disk so it can be read back the next time it starts. serialization preserves the state of the object. 
		8. What issues can occur, when using Serialization with Inner classes? 
			1. youll get an exception saying that you are trying to serialize a class that is enclosed within an outer class
		9. Where can following object relationships be used: encapsulation, association, containment, inheritance and polymorphism? 
			1. encapsulation: when you want to access instances of classes using a higher level class
			2. association: when classes have an instance of another class to use its methods. 
				3. containment: you hide the class inside another class so users cannot not even know that class exists.
					1. inner classes
			3. inheritance: when you want to share functionality of a class with another closely related class. this allows you can divide functionality between the two classes such that one only defines variables and the other class implements them.  
			4. polymorphism:  not sure.... 
		10. How can you design objects, which are self-contained and independent?
			1. 
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




