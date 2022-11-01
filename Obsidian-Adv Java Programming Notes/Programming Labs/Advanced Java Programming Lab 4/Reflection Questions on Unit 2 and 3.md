1. What role(s) does an interface play in building an API?
	1. allows developers to expose publicly and implement specific functions from another class while hiding away how the implementation happens from the user  
	2. allows two independent software components to exchange information
	3. allows multiple classes to implement the same abstract methods however they want
		1. e.g ArrayList, LinkedList, Queue classes are all lists through implemening of the List interface but they define their implementations of the abstract functions different from the other classes. 
2. What is the best way to create a framework, for exposing a complex product, in a simple way and at the same time making your implementation extensible. 
	1. CRUD operations from the backend users can perform will be exposed and implemented using interfaces
	2. ????
3. What is the advantage of exposing methods using different interfaces? 
	1. you gain data type extensibility beyond just being able to expose methods from the backend. 
		2. e.g
		3. we can see that BuildAuto **CAN** and **IS**: CreateAuto, UpdateAuto, ReadAuto, FixAuto
		4. ![[Pasted image 20221031182533.png]]
4. Is there any advantage of creating an abstract class, which contains interface method implementations only?
	1. no. if you are just using an abstract method for interface method implementation, you are losing out on the rest of an abstract class's functionality because interface implementation also has type extension
	2. abstract classes have the flexibility of being a regular class that cannot be instantiated and allowing the implementation of abstract methods
	3. for interfaces, you make use of implementation or type extension
5. How can you create a software architecture, which addresses the needs of exception handling and recovery?
	1. Create a custom exception that can be logged via a number and error message
	2. in your CRUD operations, try out your CRUD function, throw the custom exception when an error coccurs, catch it, log the error
	3. write a class that focuses on searching for and fixing the exception error
	4. expose the general functionality of the fix class with an interface
6. What is the advantage of exposing fix methods for exception management?
	1.  
7. Why did we have to make the Automobile object static in ProxyAutomotive class? 
	1. A static variable is a class variable. A single copy of the static variable is created for all instances of the class. It can be directly accessed in a static method.
	2. ![[Pasted image 20221031190326.png]]
9. What is the advantage of adding choice variable in OptionSet class? What measures had to be implemented to expose the choice property in Auto class? 
10. When implementing LinkedHashMap for Auto object in proxyAuto class, what was your consideration for managing CRUD operations on this structure? Did you end up doing the implementation of CRUD operation in proxyAuto or did you consider adding another class in Model for encapsulating Auto for the collection and then introducing an instance of this new class in proxyAuto. (Think about this and if this part of your design is not self-contained, then fix it.)